<script lang="ts">
  import { Router, Route } from "svelte-routing";
  import Header from './components/layout/Header.svelte';
  import Footer from './components/layout/Footer.svelte';
  import Home from './routes/Home.svelte';
  import Guide from './routes/Guide.svelte';
  import Prestations from './routes/Prestations.svelte';
  import Tarifs from './routes/Tarifs.svelte';
  import Pecheenfants from './routes/PecheEnfants.svelte';
  import Galerie from './routes/Galerie.svelte';
  import Videos from './routes/Videos.svelte';
  import Boutique from './routes/Boutique.svelte';
  import Montages from './routes/Montages.svelte';
  import Animations from './routes/Animations.svelte';
  import Contact from './routes/Contact.svelte';
  import Mentions from './routes/Mentions.svelte';

  export let url = "";
</script>

<Router {url}>
  <div class="flex flex-col min-h-screen">
    <Header />
    
    <main class="flex-grow">
      <Route path="/" component={Home} />
      <Route path="/guide" component={Guide} />
      <Route path="/prestations" component={Prestations} />
      <Route path="/tarifs" component={Tarifs} />
      <Route path="/peche-enfants" component={Pecheenfants} />
      <Route path="/galerie" component={Galerie} />
      <Route path="/videos" component={Videos} />
      <Route path="/boutique" component={Boutique} />
      <Route path="/montages" component={Montages} />
      <Route path="/animations" component={Animations} />
      <Route path="/contact" component={Contact} />
      <Route path="/mentions-legales" component={Mentions} />
    </main>
    
    <Footer />
  </div>
</Router>