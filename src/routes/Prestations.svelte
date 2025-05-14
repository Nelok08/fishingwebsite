<script lang="ts">
  const services = [
    {
      title: "Surfcasting",
      description: "Pêche en bord de mer avec appâts naturels ou leurres. Idéal pour bars, dorades, maigres.",
      duration: "2-4 heures",
      level: "Tous niveaux",
      season: "Toute l'année",
      equipment: "Cannes, moulinets, appâts fournis",
      image: "https://images.pexels.com/photos/5048557/pexels-photo-5048557.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=1"
    },
    {
      title: "Pêche aux leurres",
      description: "Techniques modernes pour traquer les carnassiers en eau douce et en mer.",
      duration: "2-4 heures",
      level: "Débutant à confirmé",
      season: "Mars à novembre",
      equipment: "Matériel complet fourni",
      image: "https://images.pexels.com/photos/8988935/pexels-photo-8988935.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=1"
    },
    {
      title: "Eging",
      description: "Pêche spécifique aux seiches et calamars avec techniques japonaises.",
      duration: "2-3 heures",
      level: "Tous niveaux",
      season: "Octobre à mars",
      equipment: "Matériel spécialisé fourni",
      image: "https://images.pexels.com/photos/6517765/pexels-photo-6517765.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=1"
    }
  ];
</script>

<div class="bg-gray-50 py-24">
  <div class="container-custom">
    <div class="text-center mb-16">
      <h1 class="text-4xl md:text-5xl font-bold mb-6">Nos prestations de pêche</h1>
      <p class="text-xl text-gray-600 max-w-3xl mx-auto">
        Découvrez nos différentes formules adaptées à tous les niveaux et toutes les envies
      </p>
    </div>

    <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
      {#each services as service}
        <div class="bg-white rounded-lg shadow-lg overflow-hidden">
          <img 
            src={service.image} 
            alt={service.title} 
            class="w-full h-64 object-cover"
          />
          <div class="p-6">
            <h2 class="text-2xl font-bold mb-4">{service.title}</h2>
            <p class="text-gray-600 mb-4">{service.description}</p>
            
            <div class="space-y-2 mb-6">
              <div class="flex items-center">
                <span class="font-medium w-24">Durée:</span>
                <span class="text-gray-600">{service.duration}</span>
              </div>
              <div class="flex items-center">
                <span class="font-medium w-24">Niveau:</span>
                <span class="text-gray-600">{service.level}</span>
              </div>
              <div class="flex items-center">
                <span class="font-medium w-24">Saison:</span>
                <span class="text-gray-600">{service.season}</span>
              </div>
              <div class="flex items-center">
                <span class="font-medium w-24">Matériel:</span>
                <span class="text-gray-600">{service.equipment}</span>
              </div>
            </div>
            
            <a href="/contact" class="btn-primary w-full text-center">
              Réserver
            </a>
          </div>
        </div>
      {/each}
    </div>
  </div>
</div>