<script>
    import Navbar from "$lib/components/Navbar.svelte";
    import Hero from "$lib/components/Hero.svelte";
    import About from "$lib/components/About.svelte";
    import Skills from "$lib/components/Skills.svelte";
    import Projects from "$lib/components/Projects.svelte";
    import Contact from "$lib/components/Contact.svelte";
    import Footer from "$lib/components/Footer.svelte";
</script>

<svelte:head>
    <title>Mohammed Zaid | Backend Portfolio</title>
    <meta
        name="description"
        content="Portfolio of Alex Developer, a frontend specialist."
    />
</svelte:head>

<Navbar />

<main>
    <Hero />
    <About />
    <Skills />
    <Projects />
    <Contact />
</main>

<Footer />
