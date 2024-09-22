<script>
  let gallery = [
    "../assets/images/gallery/gallery-01.jpg",
    "../assets/images/gallery/gallery-02.jpg",
    "../assets/images/gallery/gallery-03.jpg",
    "../assets/images/gallery/gallery-04.jpg",
    "../assets/images/gallery/gallery-05.jpg",
    "../assets/images/gallery/gallery-06.jpg",
  ];
  export let showModal = false;
  export let imgaModal = "";
  function handleClick(img) {
    imgaModal = img;
    showModal = true;
  }
  function closeModal() {
    showModal = false;
  }
</script>

<section class="gallery">
  <div class="gallery__lists">
    {#each gallery as img}
      <button
        class="gallery__lists-items"
        on:click={() => {
          handleClick(img);
        }}
      >
        <img src={img} alt="gallery " />
      </button>
    {/each}
  </div>
  {#if showModal}
    <div class="modal-backdrop" on:click={closeModal}></div>
    <div class="modal">
      <slot>
        <img src={imgaModal} alt="" />
      </slot>
      <button class="modal-btn" on:click={closeModal}>Close</button>
    </div>
  {/if}
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

  .modal-backdrop {
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background: rgba(0, 0, 0, 0.5);
  }
  .modal {
    position: fixed;
    display: flex;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    background: transparent;
    border-radius: 8px;
    box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
    width: calc(100% - 24px);
  }
  @media screen and (min-width: 1200px) {
    .modal {
      width: max-content;
    }
  }
  @media screen and (max-width: 540px) {
    .modal {
      width: calc(100% - 24px);
    }
  }
  .modal-btn {
    position: absolute;
    top: -10px;
    right: -10px;
    font-size: 0;
    width: 32px;
    height: 32px;
    border-radius: 50%;
  }
  .modal-btn::before,
  .modal-btn::after {
    content: "";
    position: absolute;
    top: 50%;
    left: 50%;
    width: 18px;
    height: 2px;
    background-color: #fff;
  }
  .modal-btn::before {
    transform: translate(-50%, -50%) rotate(45deg);
  }
  .modal-btn::after {
    transform: translate(-50%, -50%) rotate(-45deg);
  }
  .modal img {
    object-fit: contain;
    border-radius: 4px;
  }
  @media screen and (min-width: 1200px) {
    .modal img {
      width: auto;
      height: calc(100vh - 20px);
    }
  }
</style>
