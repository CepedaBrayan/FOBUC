<script>
  import Footer from "$lib/components/Footer.svelte";
  import OnePageHorizontalSubView from "$lib/components/OnePageHorizontalSubView.svelte";
  import SecondHeader from "$lib/components/SecondHeader.svelte";

  const modules = import.meta.glob("/static/img/donaciones/*.avif", {
    eager: true,
  });

  let images = Object.keys(modules).map((path, index) => {
    // Corrige la ruta eliminando solo `/static`
    const publicPath = path.replace("/static", "");
    return {
      src: publicPath,
      alt: `Imagen ${index + 1}`,
    };
  });
</script>

<div class="donaciones-page">
  <div class="first-subpage-wrapper">
    <SecondHeader backRoute="/authors" />
  </div>

  <OnePageHorizontalSubView className="display-images-wrapper">
    <div class="grid-title">
      <h2>DONACIÓN DE FOTOGRAFÍAS</h2>
      <hr />
    </div>
    <div class="masonry">
      {#each images as { src, alt }}
        <img {src} {alt} />
      {/each}
    </div>
  </OnePageHorizontalSubView>

  <OnePageHorizontalSubView className="footer-section">
    <Footer />
  </OnePageHorizontalSubView>
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

  .masonry img {
    width: 100%;
    height: auto;
    border-radius: 12px;
    object-fit: cover;
    box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);
    transition: transform 0.2s ease;
    display: block;
    margin-bottom: 0;
    break-inside: avoid;
  }

  .masonry img:hover {
    transform: scale(1.03);
  }

  .masonry {
    column-count: 3;
    column-gap: 0;
  }

  .grid-title h2 {
    margin-bottom: 0.5rem;
  }

  .grid-title hr {
    border: none;
    border-top: 1px solid #888;
    margin-bottom: 2rem;
  }
</style>
