<script>
  const services = [
    {
      title: 'Data Pipeline Development',
      description: 'Build robust, scalable data pipelines using modern tools and best practices',
      icon: 'M19 11H5m14 0a2 2 0 012 2v6a2 2 0 01-2 2H5a2 2 0 01-2-2v-6a2 2 0 012-2m14 0V9a2 2 0 00-2-2M5 11V9a2 2 0 012-2m0 0V5a2 2 0 012-2h6a2 2 0 012 2v2M7 7h10'
    },
    {
      title: 'Big Data Architecture',
      description: 'Design and implement scalable big data solutions for your enterprise needs',
      icon: 'M4 7v10c0 2.21 3.582 4 8 4s8-1.79 8-4V7M4 7c0 2.21 3.582 4 8 4s8-1.79 8-4M4 7c0-2.21 3.582-4 8-4s8 1.79 8 4'
    },
    {
      title: 'Data Analytics',
      description: 'Transform raw data into actionable insights with advanced analytics',
      icon: 'M9 19v-6a2 2 0 00-2-2H5a2 2 0 00-2 2v6a2 2 0 002 2h2a2 2 0 002-2zm0 0V9a2 2 0 012-2h2a2 2 0 012 2v10m-6 0a2 2 0 002 2h2a2 2 0 002-2m0 0V5a2 2 0 012-2h2a2 2 0 012 2v14a2 2 0 01-2 2h-2a2 2 0 01-2-2z'
    }
  ];
</script>

<div id="services" class="py-20 relative">
  <div class="container mx-auto px-6">
    <h2 class="text-4xl font-bold text-center text-white mb-12" data-aos="fade-down">Our Services</h2>
    <div class="grid md:grid-cols-3 gap-8">
      {#each services as service, index}
        <div class="p-6 bg-gray-800 bg-opacity-50 backdrop-blur-lg rounded-xl border border-gray-700 
                    transform hover:scale-105 transition-all duration-300"
             data-aos="fade-up" data-aos-delay={index * 100}>
          <svg class="w-12 h-12 text-blue-400 mb-4" fill="none" stroke="currentColor" viewBox="0 0 24 24">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d={service.icon}></path>
          </svg>
          <h3 class="text-xl font-semibold mb-2 text-white">{service.title}</h3>
          <p class="text-gray-300">{service.description}</p>
        </div>
      {/each}
    </div>
  </div>
</div>