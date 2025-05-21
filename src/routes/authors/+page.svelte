<script>
  import Footer from "$lib/components/Footer.svelte";
  import OnePageHorizontalSubView from "$lib/components/OnePageHorizontalSubView.svelte";
  import OnePageView from "$lib/components/OnePageView.svelte";
  import SecondHeader from "$lib/components/SecondHeader.svelte";
</script>

<div class="authors-page">
  <OnePageView>
    <div class="first-subpage-wrapper">
      <SecondHeader />
      <OnePageHorizontalSubView>
        <div class="authors-content">
          <h2>AUTORES</h2>
          <hr />

          <section class="author-section">
            <div class="author-flex">
              <div class="logo-and-text">
                <img
                  src="/img/gavassa-escudo.avif"
                  alt="Escudo Gavassa"
                  class="author-image"
                />
                <p class="credits">
                  Fotografía tomada del libro Club Campestre Bucaramanga S.A.
                  Tomo 1<br />
                  I.S.B.N. 978-628-01-0324-2
                </p>
              </div>

              <div class="author-text">
                <h3>LEGADO GAVASSA</h3>
                <p>
                  La familia Gavassa dejó una huella profunda en la memoria
                  visual de Bucaramanga gracias a su trabajo fotográfico
                  sistemático y comprometido con la documentación del desarrollo
                  urbano, social y arquitectónico de la ciudad. Su archivo
                  constituye un testimonio valioso del siglo XX en la región, en
                  el que se conservan imágenes de obras públicas, espacios
                  patrimoniales, escenas cotidianas y retratos que reflejan
                  transformaciones significativas en el territorio y en su
                  gente. Este legado fotográfico no solo representa una fuente
                  documental para el estudio histórico y urbanístico, sino
                  también una herramienta que permite resignificar la identidad
                  local y fortalecer la conexión entre el pasado y el presente.
                </p>
                <p class="see-more">
                  <a href="/gavassa">VER FOTOGRAFÍAS</a>
                </p>
              </div>
            </div>
          </section>
        </div>
      </OnePageHorizontalSubView>
    </div>
  </OnePageView>

  <OnePageView>
    <Footer />
  </OnePageView>
</div>

<style>
  .authors-page {
    font-family: sans-serif;
    background-color: #f4f4f4;
    color: #333;
    height: 100vh;

    overflow-y: scroll;
    scroll-snap-type: y mandatory;
    scroll-behavior: smooth;
    scrollbar-width: none; /* Firefox */
    -ms-overflow-style: none; /* IE y Edge */
  }

  .first-subpage-wrapper {
    position: relative;
    width: 100%;
    height: 100vh;
    overflow: hidden;
    z-index: 1;
  }

  .authors-content {
    padding: 2rem;
    height: 70vh;
  }

  .authors-content h2 {
    text-align: right;
  }

  .authors-content hr {
    border: none;
    border-top: 1px solid #888;
  }

  .author-section {
    background-color: white;
    padding: 2rem;
    border-radius: 12px;
  }

  .author-flex {
    display: flex;
    flex-wrap: wrap;
    gap: 2rem;
  }

  .author-image {
    width: 150px;
    height: auto;
  }

  .author-text {
    flex: 1;
    min-width: 280px;
  }

  .author-text h3 {
    margin-top: 0;
    font-size: 1.8rem;
  }

  .author-text p {
    text-align: justify;
    line-height: 1.6;
  }

  .see-more a {
    display: inline-block;
    margin-top: 1rem;
    text-decoration: none;
    font-weight: bold;
    border-bottom: 2px solid #333;
    color: #000;
  }

  .credits {
    font-size: 0.75rem;
    color: #777;
    margin-top: 1rem;
  }

  .logo-and-text {
    display: flex;
    flex-direction: column;
    align-items: center;
    width: 30%;
  }
</style>
