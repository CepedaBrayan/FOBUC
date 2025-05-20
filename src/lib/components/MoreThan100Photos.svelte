<script>
  export let photos = []; // Array de objetos { src, alt }
</script>

<section class="photos-section">
  <div class="section-header">
    <h2 class="title">MÁS DE 100 FOTOS</h2>
    <p class="subtitle">De la ciudad de Bucaramanga</p>
  </div>

  <div class="photos-grid">
    {#each photos as photo, i}
      <div class="photo-card {i === 0 ? 'photo-tall' : ''}">
        <img src={photo.src} alt={photo.alt} class="photo-image" />
      </div>
    {/each}
  </div>

  <div class="ver-mas">
    <p><a href="/galeria">Ver más</a></p>
  </div>
</section>

<style>
  .photos-section {
    background-color: #ffffff;
    height: 100vh;
  }

  .section-header {
    height: 20vh;
    text-align: left;
    flex-direction: column;
    justify-content: flex-start;
    align-items: center;
  }

  .ver-mas {
    text-align: center;
    height: 10vh;
  }

  .title {
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
</style>
