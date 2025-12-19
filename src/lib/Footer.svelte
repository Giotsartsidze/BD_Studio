<script lang="ts">
    const { year = new Date().getFullYear() } = $props();

    const footerLinks = [
        {
            title: 'კომპანია',
            links: [
                { label: 'ჩვენს შესახებ', href: '#about' },
                { label: 'გალერეა', href: '#gallery' },
                { label: 'კონტაქტი', href: '#contact' },
            ]
        },
        {
            title: 'სერვისები',
            links: [
                { label: 'სამზარეულოს დიზაინი', href: '#' },
                { label: '3D პროექტირება', href: '#' },
                { label: 'მონტაჟი', href: '#' },
            ]
        },
        {
            title: 'ინფორმაცია',
            links: [
                { label: 'ხშირად დასმული კითხვები', href: '#' },
                { label: 'გარანტია', href: '#' },
                { label: 'კონფიდენციალურობა', href: '#' },
            ]
        }
    ];
</script>

<footer class="footer">
    <div class="container">
        <div class="footer-content">
            <div class="footer-brand">
                <a href="#top" class="footer-logo">
                        <img src="/images/logo.jpg" alt="Babu & Dilara Logo" width="120" height="auto" />
                        <span>BD Studio</span>
                </a>
                <p class="footer-desc">
                    ექსკლუზიური სამზარეულოები, რომლებიც ქმნის სივრცეს თქვენი ოცნებებისა და საჭიროებების შესაბამისად.
                </p>
                <div class="social-links">
                    <a href="https://facebook.com" target="_blank" rel="noopener" class="social-link" aria-label="Facebook">
                        <svg width="20" height="20" viewBox="0 0 24 24" fill="currentColor">
                            <path d="M24 12.073c0-6.627-5.373-12-12-12s-12 5.373-12 12c0 5.99 4.388 10.954 10.125 11.854v-8.385H7.078v-3.47h3.047V9.43c0-3.007 1.792-4.669 4.533-4.669 1.312 0 2.686.235 2.686.235v2.953H15.83c-1.491 0-1.956.925-1.956 1.874v2.25h3.328l-.532 3.47h-2.796v8.385C19.612 23.027 24 18.062 24 12.073z"/>
                        </svg>
                    </a>
                    <a href="https://instagram.com" target="_blank" rel="noopener" class="social-link" aria-label="Instagram">
                        <svg width="20" height="20" viewBox="0 0 24 24" fill="currentColor">
                            <path d="M12 2.163c3.204 0 3.584.012 4.85.07 3.252.148 4.771 1.691 4.919 4.919.058 1.265.069 1.645.069 4.849 0 3.205-.012 3.584-.069 4.849-.149 3.225-1.664 4.771-4.919 4.919-1.266.058-1.644.07-4.85.07-3.204 0-3.584-.012-4.849-.07-3.26-.149-4.771-1.699-4.919-4.92-.058-1.265-.07-1.644-.07-4.849 0-3.204.013-3.583.07-4.849.149-3.227 1.664-4.771 4.919-4.919 1.266-.057 1.645-.069 4.849-.069zm0-2.163c-3.259 0-3.667.014-4.947.072-4.358.2-6.78 2.618-6.98 6.98-.059 1.281-.073 1.689-.073 4.948 0 3.259.014 3.668.072 4.948.2 4.358 2.618 6.78 6.98 6.98 1.281.058 1.689.072 4.948.072 3.259 0 3.668-.014 4.948-.072 4.354-.2 6.782-2.618 6.979-6.98.059-1.28.073-1.689.073-4.948 0-3.259-.014-3.667-.072-4.947-.196-4.354-2.617-6.78-6.979-6.98-1.281-.059-1.69-.073-4.949-.073zm0 5.838c-3.403 0-6.162 2.759-6.162 6.162s2.759 6.163 6.162 6.163 6.162-2.759 6.162-6.163c0-3.403-2.759-6.162-6.162-6.162zm0 10.162c-2.209 0-4-1.79-4-4 0-2.209 1.791-4 4-4s4 1.791 4 4c0 2.21-1.791 4-4 4zm6.406-11.845c-.796 0-1.441.645-1.441 1.44s.645 1.44 1.441 1.44c.795 0 1.439-.645 1.439-1.44s-.644-1.44-1.439-1.44z"/>
                        </svg>
                    </a>
                    <a href="https://linkedin.com" target="_blank" rel="noopener" class="social-link" aria-label="LinkedIn">
                        <svg width="20" height="20" viewBox="0 0 24 24" fill="currentColor">
                            <path d="M20.447 20.452h-3.554v-5.569c0-1.328-.027-3.037-1.852-3.037-1.853 0-2.136 1.445-2.136 2.939v5.667H9.351V9h3.414v1.561h.046c.477-.9 1.637-1.85 3.37-1.85 3.601 0 4.267 2.37 4.267 5.455v6.286zM5.337 7.433c-1.144 0-2.063-.926-2.063-2.065 0-1.138.92-2.063 2.063-2.063 1.14 0 2.064.925 2.064 2.063 0 1.139-.925 2.065-2.064 2.065zm1.782 13.019H3.555V9h3.564v11.452zM22.225 0H1.771C.792 0 0 .774 0 1.729v20.542C0 23.227.792 24 1.771 24h20.451C23.2 24 24 23.227 24 22.271V1.729C24 .774 23.2 0 22.222 0h.003z"/>
                        </svg>
                    </a>
                </div>
            </div>

            {#each footerLinks as section}
                <div class="footer-section">
                    <h4>{section.title}</h4>
                    <ul>
                        {#each section.links as link}
                            <li>
                                <a href={link.href}>{link.label}</a>
                            </li>
                        {/each}
                    </ul>
                </div>
            {/each}
        </div>

        <div class="footer-bottom">
            <p class="copyright">&copy; {year} BD Studio. ყველა უფლება დაცულია.</p>
            <div class="footer-bottom-links">
                <a href="#">კონფიდენციალურობა</a>
                <a href="#">წესები და პირობები</a>
            </div>
        </div>
    </div>
</footer>

<style>
    .footer {
        background: var(--primary-dark);
        color: rgba(255, 255, 255, 0.8);
        padding: 80px 0 0;
        margin-top: 0;
    }

    .footer-content {
        display: grid;
        grid-template-columns: 1.5fr 1fr 1fr 1fr;
        gap: 60px;
        padding-bottom: 60px;
        border-bottom: 1px solid rgba(255, 255, 255, 0.1);
    }

    .footer-brand {
        max-width: 350px;
    }

    .footer-logo {
        display: flex;
        align-items: center;
        gap: 12px;
        text-decoration: none;
        color: var(--text-light);
        font-family: 'Cormorant Garamond', serif;
        font-size: 1.5em;
        font-weight: 700;
        margin-bottom: 20px;
    }

    .footer-logo svg {
        color: var(--primary-gold);
    }

    .footer-desc {
        font-size: 0.95em;
        line-height: 1.7;
        color: rgba(255, 255, 255, 0.6);
        margin-bottom: 30px;
    }

    .social-links {
        display: flex;
        gap: 12px;
    }

    .social-link {
        width: 40px;
        height: 40px;
        background: rgba(255, 255, 255, 0.1);
        border-radius: 8px;
        display: flex;
        align-items: center;
        justify-content: center;
        color: rgba(255, 255, 255, 0.8);
        transition: all 0.3s ease;
        text-decoration: none;
    }

    .social-link:hover {
        background: var(--primary-gold);
        color: var(--text-light);
        transform: translateY(-3px);
    }

    .footer-section h4 {
        font-family: 'Inter', sans-serif;
        font-size: 1.1em;
        font-weight: 600;
        color: var(--text-light);
        margin-bottom: 25px;
        letter-spacing: 0.5px;
    }

    .footer-section ul {
        list-style: none;
        padding: 0;
        margin: 0;
    }

    .footer-section li {
        margin-bottom: 15px;
    }

    .footer-section a {
        color: rgba(255, 255, 255, 0.6);
        text-decoration: none;
        font-size: 0.95em;
        transition: all 0.3s ease;
    }

    .footer-section a:hover {
        color: var(--primary-gold);
        padding-left: 5px;
    }

    .footer-bottom {
        display: flex;
        justify-content: space-between;
        align-items: center;
        padding: 30px 0;
    }

    .copyright {
        font-size: 0.9em;
        color: rgba(255, 255, 255, 0.5);
        margin: 0;
    }

    .footer-bottom-links {
        display: flex;
        gap: 30px;
    }

    .footer-bottom-links a {
        color: rgba(255, 255, 255, 0.5);
        text-decoration: none;
        font-size: 0.9em;
        transition: color 0.3s ease;
    }

    .footer-bottom-links a:hover {
        color: var(--primary-gold);
    }

    @media (max-width: 1024px) {
        .footer-content {
            grid-template-columns: 1fr 1fr;
            gap: 50px;
        }

        .footer-brand {
            grid-column: 1 / -1;
            max-width: 100%;
        }
    }

    @media (max-width: 600px) {
        .footer {
            padding: 50px 0 0;
        }

        .footer-content {
            grid-template-columns: 1fr;
            gap: 40px;
            padding-bottom: 40px;
        }

        .footer-bottom {
            flex-direction: column;
            gap: 20px;
            text-align: center;
        }

        .footer-bottom-links {
            flex-direction: column;
            gap: 15px;
        }
    }
</style>