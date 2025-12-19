<script lang="ts">
    let isMenuOpen = $state(false);
    let isScrolled = $state(false);

    const navLinks = [
        { href: '#about', label: 'ჩვენს შესახებ' },
        { href: '#gallery', label: 'გალერეა' },
        { href: '#contact', label: 'კონტაქტი' },
    ];

    function toggleMenu() {
        isMenuOpen = !isMenuOpen;
    }

    if (typeof window !== 'undefined') {
        window.addEventListener('scroll', () => {
            isScrolled = window.scrollY > 50;
        });
    }
</script>

<header class="navbar" class:scrolled={isScrolled}>
    <div class="container">
        <a href="#top" class="logo">
                <img src="/images/logo.jpg" alt="Babu & Dilara Logo" width="120" height="auto" />
            <span>BD Studio</span>
        </a>

        <nav class="nav-links desktop">
            {#each navLinks as link}
                <a href={link.href} on:click={() => isMenuOpen = false}>{link.label}</a>
            {/each}
            <a href="#contact" class="nav-cta">დაგვიკავშირდით</a>
        </nav>

        <button class="menu-button" on:click={toggleMenu} aria-expanded={isMenuOpen}>
            <span></span>
            <span></span>
            <span></span>
        </button>
    </div>

    {#if isMenuOpen}
        <div class="mobile-overlay" on:click={toggleMenu}></div>
        <nav class="nav-links mobile" class:open={isMenuOpen}>
            {#each navLinks as link}
                <a href={link.href} on:click={() => isMenuOpen = false}>{link.label}</a>
            {/each}
            <a href="#contact" class="nav-cta" on:click={() => isMenuOpen = false}>უფასო კონსულტაცია</a>
        </nav>
    {/if}
</header>

<style>
    .navbar {
        position: fixed;
        top: 0;
        left: 0;
        width: 100%;
        background-color: transparent;
        z-index: 1000;
        transition: all 0.4s cubic-bezier(0.4, 0, 0.2, 1);
        padding: 20px 0;
    }

    .navbar.scrolled {
        background-color: rgba(255, 255, 255, 0.98);
        box-shadow: 0 2px 20px rgba(0, 0, 0, 0.08);
        padding: 12px 0;
        backdrop-filter: blur(10px);
    }

    .container {
        display: flex;
        justify-content: space-between;
        align-items: center;
    }

    .logo {
        display: flex;
        align-items: center;
        gap: 12px;
        text-decoration: none;
        color: var(--text-light);
        font-family: 'Cormorant Garamond', serif;
        font-size: 1.5em; /* გაზარდეთ თუ გსურთ უფრო დიდი ტექსტი */
        font-weight: 700;
        transition: all 0.3s ease;
    }

    .logo img {
        width: 40px;
        height: 40px;
        object-fit: contain;
        border-radius: 20px;
    }

    .navbar.scrolled .logo {
        color: var(--primary-dark);
    }

    .logo svg {
        color: var(--primary-gold);
    }

    .nav-links.desktop {
        display: flex;
        align-items: center;
        gap: 40px;
    }

    .nav-links.desktop a {
        text-decoration: none;
        color: var(--text-light);
        font-size: 0.95em;
        font-weight: 500;
        letter-spacing: 0.5px;
        position: relative;
        transition: all 0.3s ease;
    }

    .navbar.scrolled .nav-links.desktop a {
        color: var(--text-dark);
    }

    .nav-links.desktop a:not(.nav-cta)::after {
        content: '';
        position: absolute;
        bottom: -5px;
        left: 0;
        width: 0;
        height: 2px;
        background: var(--primary-gold);
        transition: width 0.3s ease;
    }

    .nav-links.desktop a:not(.nav-cta):hover::after {
        width: 100%;
    }

    .nav-cta {
        background: var(--primary-gold);
        color: var(--text-light) !important;
        padding: 12px 28px;
        border-radius: 4px;
        font-weight: 600;
        transition: all 0.3s ease;
    }

    .nav-cta:hover {
        background: #b89449;
        transform: translateY(-2px);
        box-shadow: 0 8px 20px rgba(201, 169, 97, 0.3);
    }

    .menu-button {
        display: none;
        flex-direction: column;
        gap: 5px;
        background: none;
        border: none;
        padding: 8px;
        cursor: pointer;
    }

    .menu-button span {
        width: 25px;
        height: 2px;
        background: var(--text-light);
        transition: all 0.3s ease;
    }

    .navbar.scrolled .menu-button span {
        background: var(--primary-dark);
    }

    .mobile-overlay {
        display: none;
    }

    .nav-links.mobile {
        display: none;
    }

    @media (max-width: 968px) {
        .nav-links.desktop {
            display: none;
        }

        .menu-button {
            display: flex;
            z-index: 1002;
        }

        .mobile-overlay {
            display: block;
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0, 0, 0, 0.5);
            z-index: 999;
            backdrop-filter: blur(5px);
        }

        .nav-links.mobile {
            display: flex;
            flex-direction: column;
            position: fixed;
            top: 0;
            right: 0;
            width: 300px;
            height: 100vh;
            background: var(--bg-white);
            padding: 100px 40px 40px;
            gap: 30px;
            box-shadow: -5px 0 30px rgba(0, 0, 0, 0.1);
            transform: translateX(100%);
            transition: transform 0.4s cubic-bezier(0.4, 0, 0.2, 1);
            z-index: 1001;
        }

        .nav-links.mobile.open {
            transform: translateX(0);
        }

        .nav-links.mobile a {
            color: var(--text-dark);
            text-decoration: none;
            font-size: 1.1em;
            font-weight: 500;
            padding: 12px 0;
            border-bottom: 1px solid var(--border-color);
        }

        .nav-links.mobile .nav-cta {
            margin-top: 20px;
            text-align: center;
            border-bottom: none;
        }
    }
</style>