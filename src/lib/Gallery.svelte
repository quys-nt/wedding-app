<script>
  import Modal from "./Modal.svelte";
  import SvelteCarousel from "./SvelteCarousel.svelte";

  let gallery = [
    "../assets/images/gallery/gallery-01.jpg",
    "../assets/images/gallery/gallery-02.jpg",
    "../assets/images/gallery/gallery-03.jpg",
    "../assets/images/gallery/gallery-04.jpg",
    "../assets/images/gallery/gallery-05.jpg",
    "../assets/images/gallery/gallery-06.jpg",
  ];

  let showModal = false;
  let selectedImageIndex = 0;

  function openModal(index) {
    selectedImageIndex = index;
    showModal = true;
  }

  function closeModal() {
    showModal = false;
  }
</script>

<section class="gallery">
  <div class="gallery__lists">
    {#each gallery as img, index}
      <button class="gallery__lists-items" on:click={() => openModal(index)}>
        <img src={img} alt="gallery" />
      </button>
    {/each}
  </div>

  <SvelteCarousel {showModal} images={gallery} onClose={closeModal} />
</section>

<style>
  .gallery {
    position: relative;
    padding: 60px 12px;
    background: url("../assets/images/bg-gallery.jpg") no-repeat top center;
    background-size: cover;
  }

  @media screen and (max-width: 768px) {
    .gallery {
      padding-block: 20px;
    }
  }

  .gallery__lists {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 10px;
    max-width: 1440px;
    margin-inline: auto;
    cursor: pointer;
  }

  @media screen and (max-width: 768px) {
    .gallery__lists {
      grid-template-columns: repeat(2, 1fr);
      gap: 6px;
    }
  }

  .gallery__lists-items {
    display: flex;
    border-radius: 4px;
    overflow: hidden;
    border: 0;
    outline: 0;
    background: transparent;
    padding: 0;
  }
</style>
