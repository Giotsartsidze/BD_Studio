<script lang="ts">
    const {
        headline = 'რატომ გვირჩევენ ჩვენ?',
        text = 'ჩვენ არ ვყიდით უბრალოდ სამზარეულოებს; ჩვენ ვქმნით ერგონომიულ, გამძლე და ესთეტიკურ სივრცეს. 10 წლიანი გამოცდილება, იტალიური მასალები და გარანტირებული ხარისხი. ჩვენ ვართ თქვენი პარტნიორები, დაწყებული იდეით დასრულებული მონტაჟით.',
    } = $props();

    const features = [
        {
            icon: '🎨',
            title: 'ინდივიდუალური დიზაინი',
            desc: 'თითოეული პროექტი უნიკალურია და შექმნილია თქვენი საჭიროებიდან გამომდინარე'
        },
        {
            icon: '🇮🇹',
            title: 'პრემიუმ ხარისხის მასალები',
            desc: 'ვიყენებთ მხოლოდ პრემიუმ ხარისხის მასალებს სანდო მომწოდებლებისგან'
        },
        {
            icon: '⚡',
            title: 'სწრაფი მონტაჟი',
            desc: 'პროფესიონალური გუნდი უზრუნველყოფს სწრაფ და ხარისხიან მონტაჟს'
        },
        {
            icon: '🛡️',
            title: '10 წლიანი გარანტია',
            desc: 'ვაძლევთ სრულ გარანტიას ჩვენს მუშაობაზე და მასალებზე'
        }
    ];
</script>

<section id="about" class="about-section">
    <div class="container">
        <div class="section-header">
            <span class="section-badge">ჩვენს შესახებ</span>
            <h2>ხარისხი დეტალებშია</h2>
        </div>

        <div class="about-grid">
            <div class="text-content">
                <h3>{headline}</h3>
                <p class="lead">{text}</p>

                <div class="features-grid">
                    {#each features as feature}
                        <div class="feature-card">
                            <span class="feature-icon">{feature.icon}</span>
                            <h4>{feature.title}</h4>
                            <p>{feature.desc}</p>
                        </div>
                    {/each}
                </div>

                <a href="#contact" class="learn-more">
                    უფასო კონსულტაცია
                    <svg width="20" height="20" viewBox="0 0 20 20" fill="none">
                        <path d="M7.5 15L12.5 10L7.5 5" stroke="currentColor" stroke-width="2" stroke-linecap="round"/>
                    </svg>
                </a>
            </div>

            <div class="image-content">
                <div class="image-wrapper">
                    <img src="https://images.unsplash.com/photo-1556911220-bff31c812dba?w=800&q=80" alt="ხარისხის მასალები" class="about-image main" />
                    <div class="image-accent"></div>
                </div>

                <div class="stats-card">
                    <div class="stat-item">
                        <span class="stat-num">500+</span>
                        <span class="stat-text">პროექტი</span>
                    </div>
                    <div class="stat-item">
                        <span class="stat-num">10</span>
                        <span class="stat-text">წელი</span>
                    </div>
                </div>
            </div>
        </div>
    </div>
</section>

<style>
    .about-section {
        background: var(--bg-white);
        position: relative;
    }

    .section-header {
        text-align: center;
        margin-bottom: 80px;
    }

    .section-badge {
        display: inline-block;
        background: rgba(176, 138, 85, 0.12);
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
        margin-bottom: 0;
    }

    .about-grid {
        display: grid;
        grid-template-columns: 1.1fr 0.9fr;
        gap: 100px;
        align-items: center;
    }

    .text-content h3 {
        font-size: 2.2em;
        line-height: 1.3;
        margin-bottom: 0.5em;
        color: var(--primary-dark);
    }

    .lead {
        font-size: 1.15em;
        line-height: 1.8;
        color: var(--text-gray);
        margin-bottom: 50px;
    }

    .features-grid {
        display: grid;
        grid-template-columns: 1fr 1fr;
        gap: 30px;
        margin-bottom: 40px;
    }

    .feature-card {
        padding: 0;
    }

    .feature-icon {
        font-size: 2.5em;
        display: block;
        margin-bottom: 15px;
    }

    .feature-card h4 {
        font-size: 1.1em;
        font-weight: 600;
        margin-bottom: 10px;
        color: var(--primary-dark);
        font-family: 'Inter', sans-serif;
    }

    .feature-card p {
        font-size: 0.95em;
        color: var(--text-gray);
        line-height: 1.6;
        margin: 0;
    }

    .learn-more {
        display: inline-flex;
        align-items: center;
        gap: 10px;
        color: var(--primary-gold);
        text-decoration: none;
        font-weight: 600;
        font-size: 1.05em;
        transition: all 0.3s ease;
        border-bottom: 2px solid transparent;
    }

    .learn-more:hover {
        gap: 15px;
        border-bottom-color: var(--primary-gold);
    }

    .image-content {
        position: relative;
    }

    .image-wrapper {
        position: relative;
        border-radius: 8px;
        overflow: hidden;
        box-shadow: 0 20px 60px rgba(0, 0, 0, 0.15);
    }

    .about-image {
        width: 100%;
        height: 600px;
        object-fit: cover;
        display: block;
    }

    .image-accent {
        position: absolute;
        top: -20px;
        right: -20px;
        width: 200px;
        height: 200px;
        background: var(--primary-gold);
        opacity: 0.1;
        border-radius: 8px;
        z-index: -1;
    }

    .stats-card {
        position: absolute;
        bottom: 40px;
        left: -40px;
        background: var(--bg-white);
        padding: 30px 40px;
        border-radius: 8px;
        box-shadow: 0 10px 40px rgba(0, 0, 0, 0.15);
        display: flex;
        gap: 50px;
    }

    .stat-item {
        display: flex;
        flex-direction: column;
        align-items: center;
        gap: 5px;
    }

    .stat-num {
        font-family: 'Cormorant Garamond', serif;
        font-size: 2.5em;
        font-weight: 700;
        color: var(--primary-gold);
        line-height: 1;
    }

    .stat-text {
        font-size: 0.9em;
        color: var(--text-gray);
        font-weight: 500;
        text-transform: uppercase;
        letter-spacing: 1px;
    }

    @media (max-width: 1024px) {
        .about-grid {
            grid-template-columns: 1fr;
            gap: 60px;
        }

        .image-content {
            order: -1;
        }

        .stats-card {
            left: 20px;
            bottom: 20px;
        }
    }

    @media (max-width: 768px) {
        .section-header h2 {
            font-size: 2em;
        }

        .text-content h3 {
            font-size: 1.8em;
        }

        .features-grid {
            grid-template-columns: 1fr;
            gap: 40px;
        }

        .about-image {
            height: 400px;
        }

        .stats-card {
            position: static;
            margin-top: 20px;
            gap: 30px;
            padding: 20px 30px;
        }
    }
</style>