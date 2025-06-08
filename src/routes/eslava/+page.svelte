<script>
  import Footer from "$lib/components/Footer.svelte";
  import OnePageHorizontalSubView from "$lib/components/OnePageHorizontalSubView.svelte";
  import SecondHeader from "$lib/components/SecondHeader.svelte";

  const modules = import.meta.glob("/static/img/eslava/*.avif", {
    eager: true,
  });

  let images = Object.keys(modules).map((path, index) => {
    const publicPath = path.replace("/static", "");
    const fileName = publicPath.split("/").pop().replace(".avif", "");
    return {
      src: publicPath,
      alt: `Imagen ${index + 1}`,
      title: fileName,
      fileName,
    };
  });

  let modalOpen = false;
  let modalSrc = "";

  function openModal(fileName) {
    modalSrc = `/img/eslava/spec-images/${fileName}.jpg`;
    modalOpen = true;
  }

  function closeModal() {
    modalOpen = false;
  }
</script>

<div class="donaciones-page">
  <div class="first-subpage-wrapper">
    <SecondHeader backRoute="/authors" />
  </div>

  <OnePageHorizontalSubView className="display-images-wrapper">
    <div class="grid-title">
      <h2>CARLOS ESLAVA FLÓREZ</h2>
      <hr />
    </div>
    <div class="masonry">
      {#each images as { src, alt, title, fileName }}
        <img {src} {alt} {title} on:click={() => openModal(fileName)} />
      {/each}
    </div>
  </OnePageHorizontalSubView>

  <OnePageHorizontalSubView className="footer-section">
    <Footer />
  </OnePageHorizontalSubView>

  {#if modalOpen}
    <div class="modal-overlay" on:click={closeModal}>
      <div class="modal-content" on:click|stopPropagation>
        <img src={modalSrc} alt="Modal image" />
        <button class="close-btn" on:click={closeModal}>×</button>
      </div>
    </div>
  {/if}
</div>

<style>
  .donaciones-page {
    font-family: sans-serif;
    background-color: #f4f4f4;
    color: #333;
    height: 100vh;
    overflow-y: scroll;
    scroll-snap-type: y mandatory;
    scroll-behavior: smooth;
    scrollbar-width: none;
    -ms-overflow-style: none;
    font-size: 0.95rem;
  }

  .donaciones-page::-webkit-scrollbar {
    display: none;
  }

  .masonry {
    column-count: 3;
    column-gap: 1rem; /* spacing between columns */
    padding: 0 1rem; /* horizontal padding inside masonry container */
  }

  .masonry img {
    width: 100%;
    height: auto;
    border-radius: 12px;
    object-fit: cover;
    box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);
    transition: transform 0.2s ease;
    display: block;
    margin-bottom: 1rem; /* spacing between images vertically */
    break-inside: avoid;
  }

  .masonry img:hover {
    transform: scale(1.03);
  }

  .grid-title h2 {
    margin-bottom: 0.5rem;
  }

  .grid-title hr {
    border: none;
    border-top: 1px solid #888;
    margin-bottom: 2rem;
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
