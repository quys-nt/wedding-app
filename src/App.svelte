<script>
  import About from "./lib/About.svelte";
  import Gallery from "./lib/Gallery.svelte";
  import MainVisual from "./lib/MainVisual.svelte";
  import SvelteCarousel from "./lib/SvelteCarousel.svelte";
</script>

<main class="main">
  <MainVisual />
  <About />
  <Gallery />
  <!-- <SvelteCarousel /> -->
</main>

<svelte:head>
  <style>
    @import url("https://fonts.googleapis.com/css2?family=Be+Vietnam+Pro:ital,wght@0,100;0,200;0,300;0,400;0,500;0,600;0,700;0,800;0,900;1,100;1,200;1,300;1,400;1,500;1,600;1,700;1,800;1,900&family=Dancing+Script:wght@400..700&family=Great+Vibes&family=Roboto+Slab:wght@100..900&display=swap");
  </style>
</svelte:head>

<style>
  .main {
    overflow: hidden;
  }
</style>
