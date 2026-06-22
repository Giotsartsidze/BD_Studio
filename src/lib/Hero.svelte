<script lang="ts">
    const {
        title = 'ავეჯი თქვენი სივრცისთვის',
        subtitle = 'პრემიუმ ხარისხი | 10 წლიანი გარანტია | უფასო პროექტირება',
        cta = 'დაჯავშნე კონსულტაცია',
        ctaSecondary = 'ნახე პროექტები'
    } = $props();
</script>

<div class="hero">
    <div class="hero-bg">
        <video
            class="hero-video"
            src="/video.mp4"
            autoplay
            muted
            loop
            playsinline
            preload="auto"
        ></video>
        <div class="hero-overlay"></div>
    </div>

    <div class="hero-content">
        <div class="container">
            <div class="hero-text">
                <span class="hero-badge">
                    <svg width="16" height="16" viewBox="0 0 16 16" fill="currentColor">
                        <path d="M8 1l2.5 5 5.5.5-4 4 1 5.5L8 13l-5 3 1-5.5-4-4 5.5-.5z"/>
                    </svg>
                    პრემიუმ ხარისხი
                </span>

                <h1>{title}</h1>
                <p class="hero-subtitle">{subtitle}</p>

                <div class="hero-stats">
                    <div class="stat">
                        <span class="stat-number">500+</span>
                        <span class="stat-label">დასრულებული პროექტი</span>
                    </div>
                    <div class="stat">
                        <span class="stat-number">98%</span>
                        <span class="stat-label">კმაყოფილი კლიენტი</span>
                    </div>
                    <div class="stat">
                        <span class="stat-number">10+</span>
                        <span class="stat-label">წლიანი გამოცდილება</span>
                    </div>
                </div>

                <div class="hero-actions">
                    <a href="#contact" class="btn btn-primary">{cta}</a>
                    <a href="#gallery" class="btn btn-secondary">{ctaSecondary}</a>
                </div>
            </div>
        </div>
    </div>

    <div class="scroll-indicator">
        <div class="mouse"></div>
    </div>
</div>

<style>
    .hero {
        position: relative;
        height: 100vh;
        min-height: 700px;
        display: flex;
        align-items: center;
        overflow: hidden;
    }

    .hero-bg {
        position: absolute;
        top: 0;
        left: 0;
        width: 100%;
        height: 100%;
        z-index: 1;
    }

    .hero-video {
        width: 100%;
        height: 100%;
        object-fit: cover;
        display: block;
    }

    .hero-overlay {
        position: absolute;
        top: 0;
        left: 0;
        width: 100%;
        height: 100%;
        background: linear-gradient(135deg, rgba(46, 32, 20, 0.85) 0%, rgba(46, 32, 20, 0.45) 60%, rgba(74, 51, 24, 0.55) 100%);
        z-index: 2;
    }

    .hero-content {
        position: relative;
        z-index: 3;
        width: 100%;
        padding-top: 80px;
    }

    .hero-text {
        max-width: 800px;
        animation: fadeInUp 1s ease-out;
    }

    @keyframes fadeInUp {
        from {
            opacity: 0;
            transform: translateY(30px);
        }
        to {
            opacity: 1;
            transform: translateY(0);
        }
    }

    .hero-badge {
        display: inline-flex;
        align-items: center;
        gap: 8px;
        background: rgba(176, 138, 85, 0.22);
        border: 1px solid rgba(176, 138, 85, 0.45);
        color: var(--primary-gold);
        padding: 8px 20px;
        border-radius: 50px;
        font-size: 0.85em;
        font-weight: 600;
        letter-spacing: 1px;
        text-transform: uppercase;
        margin-bottom: 30px;
        backdrop-filter: blur(10px);
    }

    h1 {
        font-size: 4.5em;
        color: var(--text-light);
        line-height: 1.1;
        margin-bottom: 0.3em;
        font-weight: 700;
        letter-spacing: -1px;
    }

    .hero-subtitle {
        font-size: 1.3em;
        color: rgba(255, 255, 255, 0.9);
        margin-bottom: 50px;
        font-weight: 400;
        letter-spacing: 0.5px;
    }

    .hero-stats {
        display: flex;
        gap: 60px;
        margin-bottom: 50px;
        padding: 30px 0;
        border-top: 1px solid rgba(255, 255, 255, 0.2);
        border-bottom: 1px solid rgba(255, 255, 255, 0.2);
    }

    .stat {
        display: flex;
        flex-direction: column;
        gap: 5px;
    }

    .stat-number {
        font-family: 'Cormorant Garamond', serif;
        font-size: 2.5em;
        font-weight: 700;
        color: var(--primary-gold);
        line-height: 1;
    }

    .stat-label {
        font-size: 0.9em;
        color: rgba(255, 255, 255, 0.8);
        font-weight: 500;
    }

    .hero-actions {
        display: flex;
        gap: 20px;
        flex-wrap: wrap;
    }

    .btn {
        display: inline-block;
        padding: 18px 40px;
        text-decoration: none;
        border-radius: 4px;
        font-weight: 600;
        font-size: 1em;
        letter-spacing: 0.5px;
        transition: all 0.3s ease;
        border: 2px solid transparent;
    }

    .btn-primary {
        background: var(--primary-gold);
        color: var(--text-light);
    }

    .btn-primary:hover {
        background: #96764a;
        transform: translateY(-2px);
        box-shadow: 0 10px 30px rgba(176, 138, 85, 0.45);
    }

    .btn-secondary {
        background: transparent;
        color: var(--text-light);
        border-color: rgba(255, 255, 255, 0.3);
        backdrop-filter: blur(10px);
    }

    .btn-secondary:hover {
        border-color: var(--primary-gold);
        background: rgba(176, 138, 85, 0.12);
    }

    .scroll-indicator {
        position: absolute;
        bottom: 40px;
        left: 50%;
        transform: translateX(-50%);
        z-index: 3;
    }

    .mouse {
        width: 26px;
        height: 40px;
        border: 2px solid rgba(255, 255, 255, 0.5);
        border-radius: 20px;
        position: relative;
        animation: bounce 2s ease-in-out infinite;
    }

    .mouse::before {
        content: '';
        position: absolute;
        top: 8px;
        left: 50%;
        transform: translateX(-50%);
        width: 4px;
        height: 8px;
        background: rgba(255, 255, 255, 0.8);
        border-radius: 2px;
        animation: scroll 2s ease-in-out infinite;
    }

    @keyframes bounce {
        0%, 100% { transform: translateX(-50%) translateY(0); }
        50% { transform: translateX(-50%) translateY(10px); }
    }

    @keyframes scroll {
        0% { opacity: 1; transform: translateX(-50%) translateY(0); }
        100% { opacity: 0; transform: translateX(-50%) translateY(15px); }
    }

    @media (max-width: 768px) {
        .hero {
            min-height: 600px;
        }

        h1 {
            font-size: 2.5em;
        }

        .hero-subtitle {
            font-size: 1.1em;
        }

        .hero-stats {
            flex-direction: column;
            gap: 30px;
        }

        .hero-actions {
            flex-direction: column;
        }

        .btn {
            text-align: center;
            width: 100%;
        }

        .hero-badge {
            font-size: 0.75em;
        }
    }
</style>