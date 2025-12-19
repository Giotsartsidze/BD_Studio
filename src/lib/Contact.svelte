<script lang="ts">
    // googleFormUrl აღარ გვჭირდება
    // const { googleFormUrl } = $props<{ googleFormUrl: string }>();

    // რუკის URL თბილისის მისამართით
    const mapEmbedUrl = 'https://maps.google.com/maps?q=41.791194,44.742778&hl=ka&z=16&output=embed';
</script>

<section id="contact" class="contact-section">
    <div class="container">
        <div class="section-header">
            <span class="section-badge">დაგვიკავშირდით</span>
            <h2>იპოვეთ ჩვენი ოფისი რუკაზე</h2>
            <p class="section-desc">შეგიძლიათ მოგვწეროთ, დაგვირეკოთ ან გვეწვიოთ ჩვენს ოფისში.</p>
        </div>

        <div class="contact-grid map-enabled">
            <div class="contact-info-wrapper">
                <div class="info-card">
                    <h3>საკონტაქტო ინფორმაცია</h3>

                    <div class="info-items">
                        <div class="info-item">
                            <div class="info-icon">
                                <svg width="24" height="24" viewBox="0 0 24 24" fill="none">
                                    <path d="M12 2C8.13 2 5 5.13 5 9c0 5.25 7 13 7 13s7-7.75 7-13c0-3.87-3.13-7-7-7zm0 9.5c-1.38 0-2.5-1.12-2.5-2.5s1.12-2.5 2.5-2.5 2.5 1.12 2.5 2.5-1.12 2.5-2.5 2.5z" fill="currentColor"/>
                                </svg>
                            </div>
                            <div class="info-text">
                                <span class="info-label">მისამართი</span>
                                <span class="info-value">დიდი დიღომი/3 მიკრო,10 კორპუსი</span>
                            </div>
                        </div>

                        <div class="info-item">
                            <div class="info-icon">
                                <svg width="24" height="24" viewBox="0 0 24 24" fill="none">
                                    <path d="M20 10.999h2C22 5.869 18.127 2 12.99 2v2C17.052 4 20 6.943 20 10.999z" fill="currentColor"/>
                                    <path d="M13 8c2.103 0 3 .897 3 3h2c0-3.225-1.775-5-5-5v2zm3.422 5.443a1.001 1.001 0 00-1.391.043l-2.393 2.461c-.576-.11-1.734-.471-2.926-1.66-1.192-1.193-1.553-2.354-1.66-2.926l2.459-2.394a1 1 0 00.043-1.391L6.859 3.513a1 1 0 00-1.391-.087l-2.17 1.861a1 1 0 00-.29.649c-.015.25-.301 6.172 4.291 10.766C11.305 20.707 16.323 21 17.705 21c.202 0 .326-.006.359-.008a.992.992 0 00.648-.291l1.86-2.171a.997.997 0 00-.086-1.391l-4.064-3.696z" fill="currentColor"/>
                                </svg>
                            </div>
                            <div class="info-text">
                                <span class="info-label">ტელეფონი</span>
                                <span class="info-value">+995 551 870 808 </span>
                            </div>
                        </div>

                        <div class="info-item">
                            <div class="info-icon">
                                <svg width="24" height="24" viewBox="0 0 24 24" fill="none">
                                    <path d="M20 4H4c-1.1 0-2 .9-2 2v12c0 1.1.9 2 2 2h16c1.1 0 2-.9 2-2V6c0-1.1-.9-2-2-2zm0 4l-8 5-8-5V6l8 5 8-5v2z" fill="currentColor"/>
                                </svg>
                            </div>
                            <div class="info-text">
                                <span class="info-label">ელ. ფოსტა</span>
                                <span class="info-value">info@kitchenvillage.ge</span>
                            </div>
                        </div>

                        <div class="info-item">
                            <div class="info-icon">
                                <svg width="24" height="24" viewBox="0 0 24 24" fill="none">
                                    <path d="M12 2C6.48 2 2 6.48 2 12s4.48 10 10 10 10-4.48 10-10S17.52 2 12 2zm0 18c-4.41 0-8-3.59-8-8s3.59-8 8-8 8 3.59 8 8-3.59 8-8 8zm.5-13H11v6l5.25 3.15.75-1.23-4.5-2.67z" fill="currentColor"/>
                                </svg>
                            </div>
                            <div class="info-text">
                                <span class="info-label">სამუშაო საათები</span>
                                <span class="info-value">ორშ-კვი: 10:00 - 19:00</span>
                            </div>
                        </div>
                    </div>

                    <div class="social-links">
                        <a href="https://facebook.com" target="_blank" rel="noopener" class="social-link">
                            <svg width="20" height="20" viewBox="0 0 24 24" fill="currentColor">
                                <path d="M24 12.073c0-6.627-5.373-12-12-12s-12 5.373-12 12c0 5.99 4.388 10.954 10.125 11.854v-8.385H7.078v-3.47h3.047V9.43c0-3.007 1.792-4.669 4.533-4.669 1.312 0 2.686.235 2.686.235v2.953H15.83c-1.491 0-1.956.925-1.956 1.874v2.25h3.328l-.532 3.47h-2.796v8.385C19.612 23.027 24 18.062 24 12.073z"/>
                            </svg>
                        </a>
                        <a href="https://instagram.com" target="_blank" rel="noopener" class="social-link">
                            <svg width="20" height="20" viewBox="0 0 24 24" fill="currentColor">
                                <path d="M12 2.163c3.204 0 3.584.012 4.85.07 3.252.148 4.771 1.691 4.919 4.919.058 1.265.069 1.645.069 4.849 0 3.205-.012 3.584-.069 4.849-.149 3.225-1.664 4.771-4.919 4.919-1.266.058-1.644.07-4.85.07-3.204 0-3.584-.012-4.849-.07-3.26-.149-4.771-1.699-4.919-4.92-.058-1.265-.07-1.644-.07-4.849 0-3.204.013-3.583.07-4.849.149-3.227 1.664-4.771 4.919-4.919 1.266-.057 1.645-.069 4.849-.069zm0-2.163c-3.259 0-3.667.014-4.947.072-4.358.2-6.78 2.618-6.98 6.98-.059 1.281-.073 1.689-.073 4.948 0 3.259.014 3.668.072 4.948.2 4.358 2.618 6.78 6.98 6.98 1.281.058 1.689.072 4.948.072 3.259 0 3.668-.014 4.948-.072 4.354-.2 6.782-2.618 6.979-6.98.059-1.28.073-1.689.073-4.948 0-3.259-.014-3.667-.072-4.947-.196-4.354-2.617-6.78-6.979-6.98-1.281-.059-1.69-.073-4.949-.073zM12 5.838c-3.403 0-6.162 2.759-6.162 6.162s2.759 6.163 6.162 6.163 6.162-2.759 6.162-6.163c0-3.403-2.759-6.162-6.162-6.162zm0 10.162c-2.209 0-4-1.79-4-4 0-2.209 1.791-4 4-4s4 1.791 4 4c0 2.21-1.791 4-4 4zm6.406-11.845c-.796 0-1.441.645-1.441 1.44s.645 1.44 1.441 1.44c.795 0 1.439-.645 1.439-1.44s-.644-1.44-1.439-1.44z"/>
                            </svg>
                        </a>
                    </div>
                </div>
            </div>

            <div class="map-container">
                <iframe
                        src={mapEmbedUrl}
                        width="100%"
                        height="100%"
                        style="border:0;"
                        allowfullscreen=""
                        loading="lazy"
                        referrerpolicy="no-referrer-when-downgrade"
                        title="ჩვენი მისამართი რუკაზე"
                ></iframe>
            </div>
        </div>
    </div>
</section>

<style>
    .contact-section {
        background: var(--bg-white);
        position: relative;
    }

    .section-header {
        text-align: center;
        margin-bottom: 80px;
        max-width: 700px;
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

    /* contact-grid კლასი, რომელიც აკონტროლებს საკონტაქტო ბარათისა და რუკის განლაგებას */
    .contact-grid.map-enabled {
        display: grid;
        grid-template-columns: 0.9fr 1.1fr; /* ინფო ბარათი მარცხნივ, რუკა მარჯვნივ */
        gap: 60px;
        align-items: start;
    }

    .info-card {
        background: var(--bg-light);
        padding: 50px;
        border-radius: 12px;
        position: sticky;
        top: 100px;
        box-shadow: 0 10px 40px rgba(0, 0, 0, 0.1); /* რუკასთან თანაბარი ვიზუალი */
    }

    .info-card h3 {
        font-size: 2em;
        margin-bottom: 40px;
        font-family: 'Cormorant Garamond', serif;
    }

    .info-items {
        display: flex;
        flex-direction: column;
        gap: 35px;
        margin-bottom: 50px;
    }

    .info-item {
        display: flex;
        gap: 20px;
        align-items: flex-start;
    }

    .info-icon {
        width: 50px;
        height: 50px;
        background: var(--bg-white);
        border-radius: 8px;
        display: flex;
        align-items: center;
        justify-content: center;
        color: var(--primary-gold);
        flex-shrink: 0;
    }

    .info-text {
        display: flex;
        flex-direction: column;
        gap: 5px;
    }

    .info-label {
        font-size: 0.85em;
        color: var(--text-gray);
        font-weight: 500;
        text-transform: uppercase;
        letter-spacing: 1px;
    }

    .info-value {
        font-size: 1.1em;
        color: var(--primary-dark);
        font-weight: 600;
    }

    .social-links {
        display: flex;
        gap: 15px;
        padding-top: 30px;
        border-top: 1px solid var(--border-color);
    }

    .social-link {
        width: 50px;
        height: 50px;
        background: var(--bg-white);
        border-radius: 8px;
        display: flex;
        align-items: center;
        justify-content: center;
        color: var(--text-dark);
        transition: all 0.3s ease;
        text-decoration: none;
    }

    .social-link:hover {
        background: var(--primary-gold);
        color: var(--text-light);
        transform: translateY(-3px);
    }

    /* Google Maps-ის კონტეინერი */
    .map-container {
        /* ვიყენებთ იგივე სტილებს, რაც google-form-container-ს ჰქონდა */
        background: var(--bg-light);
        border-radius: 12px;
        overflow: hidden;
        box-shadow: 0 10px 40px rgba(0, 0, 0, 0.1);
        height: 600px; /* ფიქსირებული სიმაღლე რუკისთვის */
    }

    .map-container iframe {
        display: block;
        border: none !important; /* უზრუნველყოს, რომ border არ აქვს */
        width: 100%;
        height: 100%;
    }

    /* warning-card-ის სტილები აღარ გვჭირდება */
    /* .warning-card { ... } */

    @media (max-width: 1024px) {
        .contact-grid.map-enabled {
            grid-template-columns: 1fr;
            gap: 50px;
        }

        .info-card {
            position: static;
        }

        .map-container {
            height: 400px; /* მობილურზე შედარებით დაბალი სიმაღლე */
        }
    }

    @media (max-width: 768px) {
        .section-header h2 {
            font-size: 2em;
        }

        .info-card {
            padding: 30px;
        }

        .info-card h3 {
            font-size: 1.6em;
        }
    }
</style>