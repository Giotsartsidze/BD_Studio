<script lang="ts">
    import Hero from '$lib/Hero.svelte';
    import GallerySlider from '$lib/GallerySlider.svelte';
    import About from '$lib/About.svelte';
    import Contact from '$lib/Contact.svelte';
    import Navbar from "$lib/Navbar.svelte";
    import Footer from "$lib/Footer.svelte";

    // *** შეცვალეთ ეს URL თქვენი Google Form-ის Embed კოდით ***
    const myGoogleFormUrl = "https://docs.google.com/forms/d/e/1FAIpQLS-xxxxxxxxxxxxxxxxxxxxxxxxxx/viewform?embedded=true";
</script>

<svelte:head>
    <title>BD Studio- ექსკლუზიური სამზარეულოები შეკვეთით</title>
    <meta name="description" content="იტალიური დიზაინის პრემიუმ სამზარეულოები. 10 წლიანი გარანტია, უფასო 3D პროექტირება და პროფესიონალური მონტაჟი." />
</svelte:head>

<main>
    <Navbar/>
    <Hero
            title="ექსკლუზიური სამზარეულოები შეკვეთით"
            subtitle="იტალიური დიზაინი | 10 წლიანი გარანტია | უფასო 3D პროექტირება"
            cta="დაჯავშნე კონსულტაცია"
            ctaSecondary="ნახე პროექტები"
    />
    <About />
    <GallerySlider />
    <Contact />
    <Footer/>
</main>

<style>
    main {
        min-height: 100vh;
    }
</style>