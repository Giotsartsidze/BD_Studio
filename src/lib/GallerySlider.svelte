<script lang="ts">
    import { onDestroy } from 'svelte';

    let currentSlide = $state(0);
    const intervalTime = 5000;
    let intervalId: number | undefined;

    const { images = [
        'https://images.unsplash.com/photo-1556911220-bff31c812dba?w=1400&q=80',
        'https://images.unsplash.com/photo-1556909172-54557c7e4fb7?w=1400&q=80',
        'https://images.unsplash.com/photo-1556909212-d5b604d0c90d?w=1400&q=80',
    ] } = $props();

    const titles = [
        'მოდერნული მინიმალიზმი',
        'კლასიკური ელეგანტურობა',
        'ინდუსტრიული სტილი',
    ];

    function nextSlide() {
        currentSlide = (currentSlide + 1) % images.length;
    }

    function prevSlide() {
        currentSlide = currentSlide === 0 ? images.length - 1 : currentSlide - 1;
    }

    function goToSlide(index: number) {
        currentSlide = index;
    }

    function startAutoSlide() {
        intervalId = window.setInterval(nextSlide, intervalTime);
    }

    $effect(() => {
        startAutoSlide();
        return () => {
            if (intervalId) clearInterval(intervalId);
        };
    });

    onDestroy(() => {
        if (intervalId) clearInterval(intervalId);
    });
</script>

<section id="gallery" class="gallery">
    <div class="container">
        <div class="section-header">
            <span class="section-badge">პორტფოლიო</span>
            <h2>ჩვენი დასრულებული პროექტები</h2>
            <p class="section-desc">თითოეული პროექტი არის უნიკალური ისტორია, რომელიც შექმნილია სიყვარულით და ყურადღებით</p>
        </div>

        <div class="slider-wrapper">
            <div class="slider-container">
                {#each images as image, i}
                    <div class="slide" class:active={i === currentSlide}>
                        <img src={image} alt={titles[i]} class="slide-image" />
                        <div class="slide-overlay">
                            <h3 class="slide-title">{titles[i]}</h3>
                        </div>
                    </div>
                {/each}

                <button onclick={prevSlide} class="slider-btn prev" aria-label="წინა სურათი">
                    <svg width="24" height="24" viewBox="0 0 24 24" fill="none">
                        <path d="M15 18L9 12L15 6" stroke="currentColor" stroke-width="2" stroke-linecap="round"/>
                    </svg>
                </button>
                <button onclick={nextSlide} class="slider-btn next" aria-label="შემდეგი სურათი">
                    <svg width="24" height="24" viewBox="0 0 24 24" fill="none">
                        <path d="M9 18L15 12L9 6" stroke="currentColor" stroke-width="2" stroke-linecap="round"/>
                    </svg>
                </button>
            </div>

            <div class="slider-info">
                <div class="slide-counter">
                    <span class="current">{String(currentSlide + 1).padStart(2, '0')}</span>
                    <span class="divider">/</span>
                    <span class="total">{String(images.length).padStart(2, '0')}</span>
                </div>

                <div class="dots">
                    {#each images as _, i}
                        <button
                                class="dot"
                                class:active={i === currentSlide}
                                onclick={() => goToSlide(i)}
                                aria-label={`სლაიდი ${i + 1}`}
                        ></button>
                    {/each}
                </div>
            </div>
        </div>
    </div>
</section>

<style>
    .gallery {
        background: var(--bg-light);
        position: relative;
    }

    .section-header {
        text-align: center;
        margin-bottom: 80px;
        max-width: 800px;
        margin-left: auto;
        margin-right: auto;
    }

    .section-badge {
        display: inline-block;
        background: rgba(201, 169, 97, 0.1);
        color: var(--primary-gold);
        padding: 8px 24px;
        border-radius: 50px;
        font-size: 0.85em;
        font-weight: 600;
        letter-spacing: 2px;
        text-transform: uppercase;
        margin-bottom: 20px;
    }

    .section-header h2 {
        font-size: 3em;
        margin-bottom: 0.3em;
    }

    .section-desc {
        font-size: 1.15em;
        color: var(--text-gray);
        line-height: 1.7;
        margin: 0;
    }

    .slider-wrapper {
        max-width: 1400px;
        margin: 0 auto;
    }

    .slider-container {
        position: relative;
        height: 700px;
        border-radius: 12px;
        overflow: hidden;
        box-shadow: 0 30px 80px rgba(0, 0, 0, 0.2);
    }

    .slide {
        position: absolute;
        top: 0;
        left: 0;
        width: 100%;
        height: 100%;
        opacity: 0;
        transition: opacity 0.8s ease-in-out;
        pointer-events: none;
    }

    .slide.active {
        opacity: 1;
        pointer-events: auto;
    }

    .slide-image {
        width: 100%;
        height: 100%;
        object-fit: cover;
    }

    .slide-overlay {
        position: absolute;
        bottom: 0;
        left: 0;
        right: 0;
        padding: 60px;
        background: linear-gradient(to top, rgba(0, 0, 0, 0.8) 0%, transparent 100%);
        transform: translateY(20px);
        opacity: 0;
        transition: all 0.6s ease;
    }

    .slide.active .slide-overlay {
        transform: translateY(0);
        opacity: 1;
    }

    .slide-title {
        color: var(--text-light);
        font-size: 2.5em;
        margin: 0;
        font-weight: 600;
    }

    .slider-btn {
        position: absolute;
        top: 50%;
        transform: translateY(-50%);
        background: rgba(255, 255, 255, 0.95);
        color: var(--primary-dark);
        border: none;
        width: 60px;
        height: 60px;
        border-radius: 50%;
        cursor: pointer;
        display: flex;
        align-items: center;
        justify-content: center;
        opacity: 0;
        transition: all 0.3s ease;
        z-index: 10;
        box-shadow: 0 10px 30px rgba(0, 0, 0, 0.2);
    }

    .slider-container:hover .slider-btn {
        opacity: 1;
    }

    .slider-btn:hover {
        background: var(--primary-gold);
        color: var(--text-light);
        transform: translateY(-50%) scale(1.1);
    }

    .prev {
        left: 40px;
    }

    .next {
        right: 40px;
    }

    .slider-info {
        display: flex;
        justify-content: space-between;
        align-items: center;
        margin-top: 40px;
        padding: 0 20px;
    }

    .slide-counter {
        font-family: 'Cormorant Garamond', serif;
        font-size: 1.8em;
        font-weight: 600;
        color: var(--primary-dark);
    }

    .current {
        color: var(--primary-gold);
    }

    .divider {
        margin: 0 8px;
        color: var(--text-gray);
    }

    .total {
        color: var(--text-gray);
    }

    .dots {
        display: flex;
        gap: 12px;
    }

    .dot {
        width: 12px;
        height: 12px;
        border-radius: 50%;
        background: #d0d0d0;
        border: none;
        cursor: pointer;
        transition: all 0.3s ease;
        padding: 0;
    }

    .dot:hover {
        background: #a0a0a0;
        transform: scale(1.2);
    }

    .dot.active {
        background: var(--primary-gold);
        width: 40px;
        border-radius: 6px;
    }

    @media (max-width: 1024px) {
        .slider-container {
            height: 500px;
        }

        .slide-title {
            font-size: 2em;
        }

        .slider-btn {
            width: 50px;
            height: 50px;
        }

        .prev {
            left: 20px;
        }

        .next {
            right: 20px;
        }
    }

    @media (max-width: 768px) {
        .section-header h2 {
            font-size: 2em;
        }

        .slider-container {
            height: 400px;
            border-radius: 8px;
        }

        .slide-overlay {
            padding: 30px;
        }

        .slide-title {
            font-size: 1.5em;
        }

        .slider-btn {
            width: 40px;
            height: 40px;
        }

        .slider-info {
            flex-direction: column;
            gap: 30px;
        }

        .slide-counter {
            font-size: 1.5em;
        }
    }
</style>