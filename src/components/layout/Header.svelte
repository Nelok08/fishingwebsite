<script lang="ts">
  import { onMount } from 'svelte';
  import { Link, location } from "svelte-routing";
  
  let isScrolled = false;
  let isMenuOpen = false;
  
  // Handle scroll event to add background to header
  onMount(() => {
    const handleScroll = () => {
      isScrolled = window.scrollY > 30;
    };
    
    window.addEventListener('scroll', handleScroll);
    
    return () => {
      window.removeEventListener('scroll', handleScroll);
    };
  });
  
  const toggleMenu = () => {
    isMenuOpen = !isMenuOpen;
  };
  
  const closeMenu = () => {
    if (isMenuOpen) isMenuOpen = false;
  };
  
  // Navigation links
  const navLinks = [
    { name: 'Accueil', path: '/' },
    { name: 'Guide de pêche', path: '/guide' },
    { name: 'Prestations', path: '/prestations' },
    { name: 'Tarifs', path: '/tarifs' },
    { name: 'Pêche enfants', path: '/peche-enfants' },
    { name: 'Galerie', path: '/galerie' },
    { name: 'Vidéos', path: '/videos' },
    { name: 'Boutique', path: '/boutique' },
    { name: 'Montages', path: '/montages' },
    { name: 'Animations', path: '/animations' },
    { name: 'Contact', path: '/contact' },
  ];
</script>

<header 
  class="fixed top-0 left-0 w-full z-50 transition-all duration-300"
  class:bg-white={isScrolled || isMenuOpen}
  class:bg-transparent={!isScrolled && !isMenuOpen}
  class:shadow-md={isScrolled || isMenuOpen}
>
  <div class="container-custom py-4 flex justify-between items-center">
    <!-- Logo -->
    <div class="flex items-center">
      <Link to="/">
        <span class="text-xl font-heading font-bold text-primary-700">Fishermaster</span>
      </Link>
    </div>
    
    <!-- Desktop Navigation -->
    <nav class="hidden lg:flex space-x-6">
      {#each navLinks as { name, path }}
        <div class="nav-link transition-all duration-200" class:nav-link-active={$location.pathname === path}>
          <Link to={path} on:click={closeMenu}>
            {name}
          </Link>
        </div>
      {/each}
    </nav>
    
    <!-- Mobile Menu Button -->
    <button
      class="lg:hidden flex items-center focus:outline-none"
      on:click={toggleMenu}
      aria-label={isMenuOpen ? 'Fermer le menu' : 'Ouvrir le menu'}
    >
      <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6 text-gray-800" fill="none" viewBox="0 0 24 24" stroke="currentColor">
        {#if isMenuOpen}
          <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M6 18L18 6M6 6l12 12" />
        {:else}
          <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16M4 18h16" />
        {/if}
      </svg>
    </button>
  </div>
  
  <!-- Mobile Menu -->
  {#if isMenuOpen}
    <div class="lg:hidden bg-white border-t">
      <div class="container-custom py-4">
        <nav class="flex flex-col space-y-4">
          {#each navLinks as { name, path }}
            <div class="nav-link py-2" class:nav-link-active={$location.pathname === path}>
              <Link to={path} on:click={closeMenu}>
                {name}
              </Link>
            </div>
          {/each}
        </nav>
      </div>
    </div>
  {/if}
</header>

<!-- Spacer for fixed header -->
<div class="h-16"></div>