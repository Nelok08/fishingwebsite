<script lang="ts">
  import { onMount } from 'svelte';
  import { Link } from "svelte-routing";
  import ServiceCard from '../components/ServiceCard.svelte';
  
  // Services data
  const services = [
    {
      title: 'Surfcasting',
      description: 'Pêche en bord de mer avec appâts naturels ou leurres pour bars, dorades, maigres.',
      image: 'https://images.pexels.com/photos/5048557/pexels-photo-5048557.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=1',
      link: '/prestations'
    },
    {
      title: 'Pêche aux leurres',
      description: 'Techniques modernes pour traquer les carnassiers en eau douce et en mer.',
      image: 'https://images.pexels.com/photos/8988935/pexels-photo-8988935.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=1',
      link: '/prestations'
    },
    {
      title: 'Pêche familiale',
      description: 'Initiation à la pêche pour toute la famille, moments conviviaux garantis.',
      image: 'https://images.pexels.com/photos/1463917/pexels-photo-1463917.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=1',
      link: '/peche-enfants'
    },
    {
      title: 'Eging',
      description: 'Pêche spécifique aux seiches et calamars avec techniques japonaises.',
      image: 'https://images.pexels.com/photos/6517765/pexels-photo-6517765.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=1',
      link: '/prestations'
    }
  ];
  
  let isVisible = false;
  
  onMount(() => {
    isVisible = true;
  });
</script>

<!-- Hero Section -->
<section class="relative h-screen-90 bg-gray-900 text-white">
  <div class="absolute inset-0 overflow-hidden">
    <img 
      src="https://images.pexels.com/photos/1655822/pexels-photo-1655822.jpeg?auto=compress&cs=tinysrgb&w=1600" 
      alt="Pêche au lever de soleil sur le Bassin d'Arcachon" 
      class="w-full h-full object-cover object-center"
    />
    <div class="absolute inset-0 bg-black opacity-40"></div>
  </div>
  
  <div class="absolute inset-0 flex flex-col justify-center items-center text-center p-4">
    <div class={isVisible ? 'animate-[fadeIn_1.5s_ease-out]' : 'opacity-0'}>
      <h1 class="text-5xl md:text-6xl lg:text-7xl font-bold mb-4 drop-shadow-lg">
        La pêche sur le Bassin d'Arcachon
      </h1>
      <p class="text-xl md:text-2xl mb-8 max-w-3xl mx-auto drop-shadow-md">
        Avec Fishermaster, vivez des expériences de pêche inoubliables, guidées par un professionnel passionné
      </p>
      <Link to="/contact" class="btn-primary text-lg px-8 py-4">
        Réserver une session
      </Link>
    </div>
  </div>
  
  <div class="absolute bottom-10 left-0 right-0 flex justify-center">
    <a href="#about" class="text-white animate-bounce">
      <span class="sr-only">Défiler vers le bas</span>
      <svg xmlns="http://www.w3.org/2000/svg" class="h-10 w-10" fill="none" viewBox="0 0 24 24" stroke="currentColor">
        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 14l-7 7m0 0l-7-7m7 7V3" />
      </svg>
    </a>
  </div>
</section>

<!-- About Section -->
<section id="about" class="section bg-white">
  <div class="container-custom">
    <div class="grid grid-cols-1 lg:grid-cols-2 gap-12 items-center">
      <div class="slide-up">
        <h2 class="text-3xl font-bold mb-6 text-gray-800">Sébastien Thill, <span class="text-primary-600">Guide de pêche diplômé d'État</span></h2>
        <p class="mb-4 text-lg">
          Bienvenue dans l'univers de la pêche artisanale et durable sur le Bassin d'Arcachon ! Je suis Sébastien Thill, moniteur guide de pêche diplômé d'État, passionné par mon métier et par la transmission de mon savoir-faire.
        </p>
        <p class="mb-4 text-lg">
          Depuis mon enfance, j'arpente les rives du Bassin d'Arcachon et j'ai à cœur de vous faire découvrir les techniques variées de pêche depuis le bord, en mer comme en eau douce.
        </p>
        <p class="mb-6 text-lg">
          Ma philosophie ? Une approche respectueuse de l'environnement, ludique et adaptée à chacun - enfants, adultes, débutants ou pêcheurs confirmés. Ensemble, nous vivrons des moments privilégiés au contact de la nature.
        </p>
        <div class="flex flex-wrap gap-4">
          <Link to="/guide" class="btn-primary">
            En savoir plus
          </Link>
          <Link to="/prestations" class="btn-outline">
            Découvrir mes prestations
          </Link>
        </div>
      </div>
      <div class="relative">
        <img 
          src="https://images.pexels.com/photos/5848766/pexels-photo-5848766.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=1" 
          alt="Guide de pêche en action" 
          class="rounded-lg shadow-xl w-full h-auto object-cover"
        />
        <div class="absolute -bottom-6 -left-6 bg-primary-600 text-white p-4 rounded-lg shadow-lg">
          <p class="font-bold">10+ années d'expérience</p>
          <p>Diplômé d'État</p>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- Services Section -->
<section class="section bg-gray-50">
  <div class="container-custom">
    <div class="text-center max-w-3xl mx-auto mb-12">
      <h2 class="text-3xl font-bold mb-4">Prestations de pêche</h2>
      <p class="text-lg text-gray-600">
        Je propose différentes formules adaptées à vos envies et à votre niveau. Découvrez mes prestations phares et choisissez celle qui vous correspond.
      </p>
    </div>
    
    <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-6">
      {#each services as service}
        <ServiceCard {service} />
      {/each}
    </div>
    
    <div class="text-center mt-12">
      <Link to="/prestations" class="btn-primary">
        Toutes les prestations
      </Link>
    </div>
  </div>
</section>

<!-- Testimonial Section -->
<section class="section bg-primary-700 text-white">
  <div class="container-custom">
    <div class="max-w-4xl mx-auto text-center">
      <svg class="w-12 h-12 mx-auto mb-4 text-primary-300" fill="currentColor" viewBox="0 0 24 24">
        <path d="M14.017 21v-7.391c0-5.704 3.731-9.57 8.983-10.609l.995 2.151c-2.432.917-3.995 3.638-3.995 5.849h4v10h-9.983zm-14.017 0v-7.391c0-5.704 3.748-9.57 9-10.609l.996 2.151c-2.433.917-3.996 3.638-3.996 5.849h3.983v10h-9.983z" />
      </svg>
      <blockquote class="text-2xl font-medium mb-8">
        "Une super journée de pêche avec Sébastien ! Sa passion est contagieuse et ses connaissances immenses. Mes enfants ont adoré son approche pédagogique et ont pris leurs premiers poissons ! Un moment inoubliable en famille."
      </blockquote>
      <div class="flex items-center justify-center">
        <div class="flex -space-x-2">
          <img class="inline-block h-10 w-10 rounded-full ring-2 ring-white" src="https://images.pexels.com/photos/220453/pexels-photo-220453.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=2" alt="Client testimonial" />
        </div>
        <div class="ml-4 text-left">
          <p class="font-medium">Thomas Dupont</p>
          <p class="text-primary-300">Sortie familiale - Août 2024</p>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- Call to Action -->
<section class="section bg-white">
  <div class="container-custom">
    <div class="bg-gradient-to-r from-primary-600 to-secondary-600 rounded-2xl overflow-hidden shadow-xl">
      <div class="flex flex-col lg:flex-row">
        <div class="lg:w-1/2 p-10 lg:p-16 flex flex-col justify-center">
          <h2 class="text-3xl font-bold text-white mb-6">Prêt à vivre une expérience de pêche inoubliable?</h2>
          <p class="text-white text-lg mb-8">
            Que vous soyez débutant ou confirmé, je vous accompagne sur les meilleurs spots du Bassin d'Arcachon. Matériel fourni, conseils personnalisés, moments conviviaux garantis.
          </p>
          <div class="flex flex-wrap gap-4">
            <Link to="/contact" class="btn bg-white text-primary-600 hover:bg-gray-100">
              Réserver maintenant
            </Link>
            <Link to="/tarifs" class="btn bg-transparent text-white border-2 border-white hover:bg-white/10">
              Voir les tarifs
            </Link>
          </div>
        </div>
        <div class="lg:w-1/2">
          <img 
            src="https://images.pexels.com/photos/5273000/pexels-photo-5273000.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=1" 
            alt="Pêche au coucher de soleil" 
            class="w-full h-full object-cover"
          />
        </div>
      </div>
    </div>
  </div>
</section>

<!-- Latest Blog Posts or Gallery Preview -->
<section class="section bg-gray-50">
  <div class="container-custom">
    <div class="text-center max-w-3xl mx-auto mb-12">
      <h2 class="text-3xl font-bold mb-4">Galerie des dernières prises</h2>
      <p class="text-lg text-gray-600">
        Découvrez les plus belles captures réalisées lors de nos sorties récentes sur le Bassin d'Arcachon.
      </p>
    </div>
    
    <div class="grid grid-cols-2 md:grid-cols-3 lg:grid-cols-4 gap-4">
      {#each Array(8) as _, i}
        <div class="relative overflow-hidden rounded-lg group">
          <img 
            src={`https://images.pexels.com/photos/${[5699679, 5699456, 9489444, 6791203, 6791793, 6791482, 6791393, 5825597][i]}/pexels-photo-${[5699679, 5699456, 9489444, 6791203, 6791793, 6791482, 6791393, 5825597][i]}.jpeg?auto=compress&cs=tinysrgb&w=600`} 
            alt="Capture de pêche" 
            class="w-full h-64 object-cover transition-transform duration-500 group-hover:scale-110"
          />
          <div class="absolute inset-0 bg-black bg-opacity-0 group-hover:bg-opacity-40 transition-opacity duration-300 flex items-center justify-center">
            <Link to="/galerie" class="opacity-0 group-hover:opacity-100 transition-opacity duration-300 btn bg-white/80 text-primary-600 hover:bg-white">
              Voir plus
            </Link>
          </div>
        </div>
      {/each}
    </div>
    
    <div class="text-center mt-12">
      <Link to="/galerie" class="btn-primary">
        Toute la galerie
      </Link>
    </div>
  </div>
</section>