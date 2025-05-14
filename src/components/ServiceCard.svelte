<script lang="ts">
  import { Link } from "svelte-routing";
  
  export let service: {
    title: string;
    description: string;
    image: string;
    link: string;
  };
</script>

<div class="card group">
  <div class="relative overflow-hidden h-56">
    <img 
      src={service.image} 
      alt={service.title} 
      class="w-full h-full object-cover transition-transform duration-500 group-hover:scale-110"
    />
    <div class="absolute inset-0 bg-gradient-to-t from-black/70 to-transparent"></div>
    <h3 class="absolute bottom-4 left-4 text-xl font-bold text-white">{service.title}</h3>
  </div>
  <div class="p-6">
    <p class="text-gray-600 mb-4">{service.description}</p>
    <Link to={service.link} class="text-primary-600 font-medium hover:text-primary-800 flex items-center">
      En savoir plus
      <svg xmlns="http://www.w3.org/2000/svg" class="h-4 w-4 ml-1" viewBox="0 0 20 20" fill="currentColor">
        <path fill-rule="evenodd" d="M12.293 5.293a1 1 0 011.414 0l4 4a1 1 0 010 1.414l-4 4a1 1 0 01-1.414-1.414L14.586 11H3a1 1 0 110-2h11.586l-2.293-2.293a1 1 0 010-1.414z" clip-rule="evenodd" />
      </svg>
    </Link>
  </div>
</div>