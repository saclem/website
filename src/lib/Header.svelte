<script>
  import { onMount } from 'svelte';
  let isMenuOpen = false;
  let scrolled = false;
  
  const toggleMenu = () => isMenuOpen = !isMenuOpen;
  
  const menuItems = [
    { href: '#home', text: 'Home' },
    { href: '#about', text: 'About' },
    { href: '#services', text: 'Services' },
    { href: '#contact', text: 'Contact' }
  ];

  onMount(() => {
    const handleScroll = () => {
      scrolled = window.scrollY > 20;
    };
    
    window.addEventListener('scroll', handleScroll);
    return () => window.removeEventListener('scroll', handleScroll);
  });
</script>

<header class="fixed w-full z-50 transition-all duration-300" class:bg-gray-900={scrolled} class:bg-opacity-80={scrolled} class:backdrop-blur-lg={scrolled}>
  <nav class="container mx-auto px-6 py-4">
    <div class="flex items-center justify-between">
      <div class="text-xl font-bold text-white">Data Engineering</div>
      
      <button class="md:hidden text-white p-2" on:click={toggleMenu} aria-label="Toggle menu">
        <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24">
          <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" 
            d={isMenuOpen ? "M6 18L18 6M6 6l12 12" : "M4 6h16M4 12h16M4 18h16"}
          />
        </svg>
      </button>

      <div class="hidden md:flex space-x-8">
        {#each menuItems as item}
          <a href={item.href} 
             class="text-gray-300 hover:text-blue-400 transition-colors">
            {item.text}
          </a>
        {/each}
      </div>
    </div>

    {#if isMenuOpen}
      <div class="md:hidden mt-4 bg-gray-900 bg-opacity-95 rounded-lg p-4">
        {#each menuItems as item}
          <a href={item.href} 
             class="block py-2 text-gray-300 hover:text-blue-400 transition-colors"
             on:click={toggleMenu}>
            {item.text}
          </a>
        {/each}
      </div>
    {/if}
  </nav>
</header>