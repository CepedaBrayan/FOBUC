<script>
  export let photos = []; // Array de objetos { src, alt }

  let modalOpen = false;
  let modalSrc = "";

  function openModal(fileName) {
    modalSrc = `/img/more-than/spec-images/${fileName}.jpg`;
    modalOpen = true;
  }

  function closeModal() {
    modalOpen = false;
  }
</script>

<section class="photos-section">
  <div class="section-header">
    <h2 class="title">MÁS DE 100 FOTOS</h2>
    <p class="subtitle">De la ciudad de Bucaramanga</p>
  </div>

  <div class="photos-grid">
    {#each photos as photo, i}
      <div class="photo-card {i === 0 ? 'photo-tall' : ''}">
        <img
          src={photo.src}
          class="photo-image"
          on:click={() => openModal(photo.alt)}
        />
      </div>
    {/each}
  </div>

  {#if modalOpen}
    <div class="modal-overlay" on:click={closeModal}>
      <div class="modal-content" on:click|stopPropagation>
        <img src={modalSrc} alt="Modal image" />
        <button class="close-btn" on:click={closeModal}>×</button>
      </div>
    </div>
  {/if}
</section>

<style>
  .photos-section {
    background-color: #ffffff;
    height: 100vh;
  }

  .section-header {
    height: 20vh;
    text-align: left;
  }

  .title {
    padding-top: 5vh;
    font-size: 36px;
    font-weight: bold;
    text-transform: uppercase;
    margin: 0;
  }

  .subtitle {
    font-size: 18px;
    color: #555;
    text-transform: uppercase;
  }

  .photos-grid {
    border-top: 3px solid #333;
    height: 70vh;
    display: grid;
    grid-template-columns: repeat(4, 1fr);
    padding: 1rem;
    gap: 1rem; /* <-- Añadido */
  }

  .photo-card {
    background: #fff;
    box-shadow: 0 1px 4px rgba(0, 0, 0, 0.15);
    border-radius: 4px;
    overflow: hidden;
    display: flex;
    flex-direction: column;
  }

  .photo-image {
    width: 100%;
    height: 100%;
    display: block;
    object-fit: cover;
    object-position: 50% 40%;
  }

  .photo-tall {
    grid-row: span 2;
  }

  .modal-overlay {
    position: fixed;
    top: 0;
    left: 0;
    width: 100vw;
    height: 100vh;
    background: rgba(0, 0, 0, 0.7);
    display: flex;
    align-items: center;
    justify-content: center;
    z-index: 1000;
  }

  .modal-content {
    position: relative;
    background: white;
    padding: 1rem;
    border-radius: 12px;
    max-width: 90vw;
    max-height: 90vh;
    display: flex;
    flex-direction: column;
    align-items: center;
  }

  .modal-content img {
    max-width: 100%;
    max-height: 90vh;
    border-radius: 8px;
  }

  .close-btn {
    position: absolute;
    top: 0.5rem;
    right: 0.75rem;
    font-size: 1.5rem;
    background: none;
    border: none;
    cursor: pointer;
    color: #333;
  }
</style>
