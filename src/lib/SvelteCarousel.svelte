<script>
  let gallery = [
    "../assets/images/gallery/gallery-01.jpg",
    "../assets/images/gallery/gallery-02.jpg",
    "../assets/images/gallery/gallery-03.jpg",
    "../assets/images/gallery/gallery-04.jpg",
    "../assets/images/gallery/gallery-05.jpg",
    "../assets/images/gallery/gallery-06.jpg",
  ];
  import Carousel from "svelte-carousel";

  let carousel;

  export let showModal = false;
  export let images = [];
  export let onClose;

  function handleBackdropClick() {
    onClose();
  }
</script>

{#if showModal}
  <div class="carousel-backdrop" on:click={handleBackdropClick}></div>
  <div class="carousel-modal">
    <Carousel dots={false} arrows={false} bind:this={carousel}>
      {#each images as imgSrc}
        <div class="carousel-modal__items">
          <img src={imgSrc} alt="gallery" />
        </div>
      {/each}
    </Carousel>
  </div>
{/if}

<style>
  .carousel-modal {
    position: fixed;
    width: 100%;
    max-width: 1212px;
    max-height: min-content;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    background: transparent;
    padding: 10px;
    border-radius: 8px;
    z-index: 100;
  }
  @media screen and (min-width: 1024px) {
    .carousel-modal {
      height: calc(100% - 24px);
    }
  }
  .carousel-backdrop {
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background: rgba(0, 0, 0, 0.5);
  }
  .carousel-modal__items {
    cursor: pointer;
  }
  .carousel-modal__items img {
    pointer-events: none;
    width: 100%;
    height: 100%;
    object-fit: contain;
  }
  .carousel-modal .sc-carousel__carousel-container {
    height: 100%;
  }
</style>
