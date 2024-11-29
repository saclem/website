<script>
  import ParticlesBackground from './ParticlesBackground.svelte';
</script>

<section id="home" class="relative min-h-screen flex items-center justify-center overflow-hidden py-20">
  <ParticlesBackground />
  
  <div class="relative z-10 text-center px-4 mt-16">
    <h1 class="text-5xl md:text-7xl font-bold text-white mb-6" data-aos="fade-down">
      Data Engineering
      <span class="block text-blue-400">Solutions</span>
    </h1>
    <p class="text-xl md:text-2xl text-gray-300 mb-8 max-w-2xl mx-auto" data-aos="fade-up" data-aos-delay="200">
      Transform your data infrastructure with modern engineering practices and cutting-edge technologies
    </p>
    <a href="#services" 
       class="inline-block bg-blue-500 text-white px-8 py-3 rounded-lg font-semibold 
              hover:bg-blue-600 transition-all transform hover:scale-105"
       data-aos="fade-up" data-aos-delay="400">
      Explore Our Services
    </a>
  </div>
</section>