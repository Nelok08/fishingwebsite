<script lang="ts">
  // Testimonials data
  const testimonials = [
    {
      text: "Sébastien est un excellent guide, patient et pédagogue. J'ai appris énormément en une seule session !",
      name: "Michel Dupont",
      date: "Juin 2024"
    },
    {
      text: "Un professionnel passionné qui partage son amour de la pêche et du Bassin d'Arcachon. Moment inoubliable !",
      name: "Sophie Martin",
      date: "Mai 2024"
    },
    {
      text: "Mes enfants ont été conquis ! Approche ludique et adaptée, ils ont pris leurs premiers poissons.",
      name: "Julien Petit",
      date: "Avril 2024"
    }
  ];
</script>

<div class="bg-gray-50 py-24">
  <div class="container-custom">
    <div class="text-center mb-16">
      <h1 class="text-4xl md:text-5xl font-bold mb-6">Sébastien Thill</h1>
      <p class="text-xl text-gray-600 max-w-3xl mx-auto">Guide de pêche diplômé d'État sur le Bassin d'Arcachon</p>
    </div>
    
    <!-- Bio Section -->
    <div class="grid grid-cols-1 lg:grid-cols-2 gap-12 mb-20">
      <div class="relative">
        <img 
          src="https://images.pexels.com/photos/5848766/pexels-photo-5848766.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=1" 
          alt="Sébastien Thill, guide de pêche" 
          class="rounded-lg shadow-lg w-full h-auto"
        />
        <div class="absolute -bottom-8 -right-8 bg-white p-6 rounded-lg shadow-xl hidden md:block">
          <img 
            src="https://images.pexels.com/photos/2131976/pexels-photo-2131976.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=1" 
            alt="En action de pêche" 
            class="w-48 h-32 object-cover rounded"
          />
        </div>
      </div>
      
      <div class="flex flex-col justify-center">
        <h2 class="text-3xl font-bold mb-6 text-gray-800">Mon parcours</h2>
        <p class="mb-4 text-lg">
          Natif de la région, j'ai grandi au bord de l'eau avec une canne à pêche dans les mains. Cette passion ne m'a jamais quitté et m'a naturellement conduit à devenir guide de pêche professionnel.
        </p>
        <p class="mb-4 text-lg">
          Titulaire du BPJEPS pêche de loisir, je suis officiellement moniteur guide de pêche, un titre qui garantit mon expertise technique et ma connaissance des milieux aquatiques.
        </p>
        <p class="mb-6 text-lg">
          Mon terrain de jeu favori ? Le magnifique Bassin d'Arcachon et ses environs, que je connais comme ma poche après des années d'exploration et de pêche sur ses rives.
        </p>
        
        <div class="grid grid-cols-2 sm:grid-cols-3 gap-4 mt-6">
          <div class="bg-white p-4 rounded-lg shadow-md text-center">
            <p class="text-3xl font-bold text-primary-600">10+</p>
            <p class="text-gray-600">Années d'expérience</p>
          </div>
          <div class="bg-white p-4 rounded-lg shadow-md text-center">
            <p class="text-3xl font-bold text-primary-600">7</p>
            <p class="text-gray-600">Techniques maîtrisées</p>
          </div>
          <div class="bg-white p-4 rounded-lg shadow-md text-center">
            <p class="text-3xl font-bold text-primary-600">100%</p>
            <p class="text-gray-600">Satisfaction client</p>
          </div>
        </div>
      </div>
    </div>
    
    <!-- Philosophy Section -->
    <div class="bg-white rounded-2xl shadow-lg p-8 md:p-12 mb-20">
      <div class="text-center mb-10">
        <h2 class="text-3xl font-bold mb-4">Ma philosophie</h2>
        <p class="text-lg text-gray-600 max-w-3xl mx-auto">
          Au-delà de la simple activité de pêche, je souhaite vous faire vivre une expérience complète de reconnexion avec la nature.
        </p>
      </div>
      
      <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
        <div class="text-center">
          <div class="bg-primary-50 w-16 h-16 rounded-full flex items-center justify-center mx-auto mb-4">
            <svg xmlns="http://www.w3.org/2000/svg" class="h-8 w-8 text-primary-600" fill="none" viewBox="0 0 24 24" stroke="currentColor">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M13 10V3L4 14h7v7l9-11h-7z" />
            </svg>
          </div>
          <h3 class="text-xl font-bold mb-2">Transmission du savoir</h3>
          <p class="text-gray-600">
            Je partage mes connaissances et techniques avec pédagogie, pour que vous progressiez à votre rythme.
          </p>
        </div>
        
        <div class="text-center">
          <div class="bg-nature-50 w-16 h-16 rounded-full flex items-center justify-center mx-auto mb-4">
            <svg xmlns="http://www.w3.org/2000/svg" class="h-8 w-8 text-nature-600" fill="none" viewBox="0 0 24 24" stroke="currentColor">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3.055 11H5a2 2 0 012 2v1a2 2 0 002 2 2 2 0 012 2v2.945M8 3.935V5.5A2.5 2.5 0 0010.5 8h.5a2 2 0 012 2 2 2 0 104 0 2 2 0 012-2h1.064M15 20.488V18a2 2 0 012-2h3.064M21 12a9 9 0 11-18 0 9 9 0 0118 0z" />
            </svg>
          </div>
          <h3 class="text-xl font-bold mb-2">Respect de l'environnement</h3>
          <p class="text-gray-600">
            Je sensibilise à la préservation des milieux aquatiques et pratique une pêche responsable.
          </p>
        </div>
        
        <div class="text-center">
          <div class="bg-accent-50 w-16 h-16 rounded-full flex items-center justify-center mx-auto mb-4">
            <svg xmlns="http://www.w3.org/2000/svg" class="h-8 w-8 text-accent-600" fill="none" viewBox="0 0 24 24" stroke="currentColor">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M14.828 14.828a4 4 0 01-5.656 0M9 10h.01M15 10h.01M21 12a9 9 0 11-18 0 9 9 0 0118 0z" />
            </svg>
          </div>
          <h3 class="text-xl font-bold mb-2">Plaisir avant tout</h3>
          <p class="text-gray-600">
            Je crée une ambiance conviviale où le plaisir et la découverte priment sur le tableau de pêche.
          </p>
        </div>
      </div>
    </div>
    
    <!-- Expertise Section -->
    <div class="mb-20">
      <div class="text-center mb-10">
        <h2 class="text-3xl font-bold mb-4">Mon expertise</h2>
        <p class="text-lg text-gray-600 max-w-3xl mx-auto">
          Je vous propose une approche adaptée à votre niveau et à vos envies, quelle que soit la technique qui vous intéresse.
        </p>
      </div>
      
      <div class="grid grid-cols-1 md:grid-cols-2 gap-8">
        <div class="bg-white rounded-lg shadow-md overflow-hidden">
          <img 
            src="https://images.pexels.com/photos/5048557/pexels-photo-5048557.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=1" 
            alt="Surfcasting" 
            class="w-full h-56 object-cover"
          />
          <div class="p-6">
            <h3 class="text-xl font-bold mb-2">Pêche en mer</h3>
            <ul class="space-y-2">
              <li class="flex items-start">
                <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5 text-primary-600 mr-2 mt-0.5" viewBox="0 0 20 20" fill="currentColor">
                  <path fill-rule="evenodd" d="M10 18a8 8 0 100-16 8 8 0 000 16zm3.707-9.293a1 1 0 00-1.414-1.414L9 10.586 7.707 9.293a1 1 0 00-1.414 1.414l2 2a1 1 0 001.414 0l4-4z" clip-rule="evenodd" />
                </svg>
                <span>Surfcasting et pêche à soutenir</span>
              </li>
              <li class="flex items-start">
                <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5 text-primary-600 mr-2 mt-0.5" viewBox="0 0 20 20" fill="currentColor">
                  <path fill-rule="evenodd" d="M10 18a8 8 0 100-16 8 8 0 000 16zm3.707-9.293a1 1 0 00-1.414-1.414L9 10.586 7.707 9.293a1 1 0 00-1.414 1.414l2 2a1 1 0 001.414 0l4-4z" clip-rule="evenodd" />
                </svg>
                <span>Pêche aux leurres en mer</span>
              </li>
              <li class="flex items-start">
                <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5 text-primary-600 mr-2 mt-0.5" viewBox="0 0 20 20" fill="currentColor">
                  <path fill-rule="evenodd" d="M10 18a8 8 0 100-16 8 8 0 000 16zm3.707-9.293a1 1 0 00-1.414-1.414L9 10.586 7.707 9.293a1 1 0 00-1.414 1.414l2 2a1 1 0 001.414 0l4-4z" clip-rule="evenodd" />
                </svg>
                <span>Eging (pêche aux céphalopodes)</span>
              </li>
              <li class="flex items-start">
                <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5 text-primary-600 mr-2 mt-0.5" viewBox="0 0 20 20" fill="currentColor">
                  <path fill-rule="evenodd" d="M10 18a8 8 0 100-16 8 8 0 000 16zm3.707-9.293a1 1 0 00-1.414-1.414L9 10.586 7.707 9.293a1 1 0 00-1.414 1.414l2 2a1 1 0 001.414 0l4-4z" clip-rule="evenodd" />
                </svg>
                <span>Techniques spécifiques au Bassin d'Arcachon</span>
              </li>
            </ul>
          </div>
        </div>
        
        <div class="bg-white rounded-lg shadow-md overflow-hidden">
          <img 
            src="https://images.pexels.com/photos/8988935/pexels-photo-8988935.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=1" 
            alt="Pêche en eau douce" 
            class="w-full h-56 object-cover"
          />
          <div class="p-6">
            <h3 class="text-xl font-bold mb-2">Pêche en eau douce</h3>
            <ul class="space-y-2">
              <li class="flex items-start">
                <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5 text-primary-600 mr-2 mt-0.5" viewBox="0 0 20 20" fill="currentColor">
                  <path fill-rule="evenodd" d="M10 18a8 8 0 100-16 8 8 0 000 16zm3.707-9.293a1 1 0 00-1.414-1.414L9 10.586 7.707 9.293a1 1 0 00-1.414 1.414l2 2a1 1 0 001.414 0l4-4z" clip-rule="evenodd" />
                </svg>
                <span>Pêche au coup et à l'anglaise</span>
              </li>
              <li class="flex items-start">
                <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5 text-primary-600 mr-2 mt-0.5" viewBox="0 0 20 20" fill="currentColor">
                  <path fill-rule="evenodd" d="M10 18a8 8 0 100-16 8 8 0 000 16zm3.707-9.293a1 1 0 00-1.414-1.414L9 10.586 7.707 9.293a1 1 0 00-1.414 1.414l2 2a1 1 0 001.414 0l4-4z" clip-rule="evenodd" />
                </svg>
                <span>Pêche aux leurres (carnassiers)</span>
              </li>
              <li class="flex items-start">
                <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5 text-primary-600 mr-2 mt-0.5" viewBox="0 0 20 20" fill="currentColor">
                  <path fill-rule="evenodd" d="M10 18a8 8 0 100-16 8 8 0 000 16zm3.707-9.293a1 1 0 00-1.414-1.414L9 10.586 7.707 9.293a1 1 0 00-1.414 1.414l2 2a1 1 0 001.414 0l4-4z" clip-rule="evenodd" />
                </svg>
                <span>Pêche au feeder</span>
              </li>
              <li class="flex items-start">
                <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5 text-primary-600 mr-2 mt-0.5" viewBox="0 0 20 20" fill="currentColor">
                  <path fill-rule="evenodd" d="M10 18a8 8 0 100-16 8 8 0 000 16zm3.707-9.293a1 1 0 00-1.414-1.414L9 10.586 7.707 9.293a1 1 0 00-1.414 1.414l2 2a1 1 0 001.414 0l4-4z" clip-rule="evenodd" />
                </svg>
                <span>Initiation pour enfants et familles</span>
              </li>
            </ul>
          </div>
        </div>
      </div>
    </div>
    
    <!-- Testimonials Section -->
    <div class="bg-white rounded-2xl shadow-lg p-8 md:p-12">
      <div class="text-center mb-10">
        <h2 class="text-3xl font-bold mb-4">Témoignages</h2>
        <p class="text-lg text-gray-600 max-w-3xl mx-auto">
          Découvrez ce que mes clients disent de leur expérience de pêche avec moi.
        </p>
      </div>
      
      <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
        {#each testimonials as testimonial}
          <div class="bg-gray-50 rounded-lg p-6 shadow">
            <svg class="w-8 h-8 text-primary-500 mb-4" fill="currentColor" viewBox="0 0 24 24">
              <path d="M14.017 21v-7.391c0-5.704 3.731-9.57 8.983-10.609l.995 2.151c-2.432.917-3.995 3.638-3.995 5.849h4v10h-9.983zm-14.017 0v-7.391c0-5.704 3.748-9.57 9-10.609l.996 2.151c-2.433.917-3.996 3.638-3.996 5.849h3.983v10h-9.983z" />
            </svg>
            <p class="text-gray-700 mb-6">"{testimonial.text}"</p>
            <div class="flex items-center mt-auto">
              <div class="ml-3">
                <p class="font-medium">{testimonial.name}</p>
                <p class="text-sm text-gray-500">{testimonial.date}</p>
              </div>
            </div>
          </div>
        {/each}
      </div>
    </div>
  </div>
</div>