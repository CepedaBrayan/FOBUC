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
      <OnePageHorizontalSubView className="fifty-fifty">
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

  <!-- Sección con autores adicionales (Platarrueda y más si se desea) -->
  <OnePageView>
    <!-- Primer autor: Andrés Platarrueda -->
    <OnePageHorizontalSubView className="fifty-fifty">
      <div class="authors-content">
        <section class="author-section">
          <div class="author-flex">
            <div class="logo-and-text">
              <img
                src="/img/platarrueda.avif"
                alt="Andrés Platarrueda"
                class="author-image"
              />
              <p class="credits">
                Fotografía tomada de<br />
                Andrés Platarrueda – Fotografía histórica de Santander.<br />
                [Fotografía antigua de Bucaramanga en 1940 publicada en su perfil
                personal]<br />
                [Fotografía]. Facebook.
              </p>
            </div>

            <div class="author-text">
              <h3>ANDRÉS PLATARRUEDA</h3>
              <p><strong>NACIMIENTO:</strong> 1926</p>
              <p>
                Destacado fotógrafo, pintor y cineasta que documentó con agudeza
                la transformación urbana y cultural de Bucaramanga. Inició su
                camino en la imagen durante el Bogotazo de 1948, al adquirir su
                primera cámara. En 1960 se estableció como fotógrafo profesional
                en la capital santandereana. Su proyecto “Ciudad Bonita: Ayer,
                Hoy y Siempre” es un valioso archivo visual del desarrollo
                regional. Además, incursionó en el cine silente y la pintura,
                dejando una huella en las artes locales. Su legado es clave en
                la memoria gráfica del oriente colombiano.
              </p>
              <p class="see-more">
                <a href="/platarrueda">VER FOTOGRAFÍAS</a>
              </p>
            </div>
          </div>
        </section>
      </div>
    </OnePageHorizontalSubView>

    <OnePageHorizontalSubView className="fifty-fifty">
      <div class="authors-content">
        <section class="author-section">
          <div class="author-flex">
            <div class="logo-and-text">
              <img
                src="/img/carlos-eslava.avif"
                alt="Carlos Eslava Flórez"
                class="author-image"
              />
              <p class="credits">
                Fotografía tomada de<br />
                Gómez, Ó. H. (2020, 28 de diciembre). El día en que Horst Martin
                Schutkowski fotografió a Capitanejo. Óscar Humberto Gómez.
              </p>
            </div>

            <div class="author-text">
              <h3>CARLOS ESLAVA FLÓREZ</h3>
              <p><strong>1935–2014</strong></p>
              <p>
                Fue un fotógrafo, periodista y compositor nacido en Pamplona,
                Norte de Santander. Aprendió fotografía en El Socorro con
                Gustavo Molina, discípulo de Leo Matiz. En 1956 se trasladó a
                Bucaramanga, donde trabajó en Foto Astro y colaboró con medios
                como Vanguardia Liberal, El Tiempo y El Espectador. Durante más
                de 60 años documentó la transformación social y urbana de
                Santander. También fue compositor, con más de 80 obras
                registradas en SAYCO. Su trabajo refleja el sentir y la
                identidad del oriente colombiano. Parte de su legado fotográfico
                se conserva en el Banco de la República.
              </p>
              <p class="see-more">
                <a href="/eslava">VER FOTOGRAFÍAS</a>
              </p>
            </div>
          </div>
        </section>
      </div>
    </OnePageHorizontalSubView>
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
    font-size: 0.95rem;
  }

  .authors-page::-webkit-scrollbar {
    display: none; /* Chrome/Safari */
  }

  .first-subpage-wrapper {
    height: 100%;
  }

  .authors-content {
    padding: 1rem;
    width: 100%;
    height: 60%;
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
    padding: 1rem;
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
    margin-top: 0.5rem;
    text-decoration: none;
    font-weight: bold;
    border-bottom: 2px solid #333;
    color: #000;
  }

  .credits {
    font-size: 0.75rem;
    color: #777;
  }

  .logo-and-text {
    display: flex;
    flex-direction: column;
    align-items: center;
    width: 20%;
  }
</style>
