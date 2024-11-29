<script>
  import { onMount } from 'svelte';
  import AOS from 'aos';
  import 'aos/dist/aos.css';
  
  import Header from './lib/Header.svelte';
  import Hero from './lib/Hero.svelte';
  import About from './lib/About.svelte';
  import Services from './lib/Services.svelte';
  import Contact from './lib/Contact.svelte';
  import Footer from './lib/Footer.svelte';

  onMount(() => {
    AOS.init({
      duration: 1000,
      once: true,
      offset: 50
    });
  });
</script>

<main class="relative">
  <Header />
  <Hero />
  <About />
  <Services />
  <Contact />
  <Footer />
</main>