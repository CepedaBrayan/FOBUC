<script>
  import Carousel from "$lib/components/Carousel.svelte";
  import Navbar from "$lib/components/Navbar.svelte";
  import OnePageHorizontalSubView from "$lib/components/OnePageHorizontalSubView.svelte";
  import OnePageView from "$lib/components/OnePageView.svelte";
</script>

<header>
  <Navbar />
  <Carousel />
</header>

<main>
  <!-- First section: article and team -->
  <OnePageView>
    <OnePageHorizontalSubView className="city-and-memory-section">
      <article>
        <h2>CIUDAD Y MEMORIA: FOTOGRAFÍA HISTÓRICA DE BUCARAMANGA</h2>
        <p>
          Este sitio web es el resultado de un proyecto académico desarrollado
          como proyecto de grado por estudiantes universitarios, cuyo propósito
          es investigar, recopilar y difundir fotografías históricas que
          documentan el desarrollo urbano, arquitectónico y social de la ciudad
          de Bucaramanga.
          <br /><br />
          El archivo reúne fotografías provenientes de distintos archivos y colecciones,
          nacionales e internacionales, con el fin de facilitar el acceso visual
          a la memoria de una ciudad en transformación.
          <br /><br />
          Este es un proyecto estrictamente académico, sin fines comerciales ni de
          lucro. Todas las fuentes han sido citadas y se ha procurado e intentado
          solicitar autorización cuando ha sido requerida.
        </p>
      </article>

      <figure>
        <img src="/img/right-lateral.avif" alt="" />
        <figcaption>
          Autor: Carlos Eslava Florez<br />
          Fuente: Banco de la República, Biblioteca Virtual
        </figcaption>
      </figure>
    </OnePageHorizontalSubView>

    <OnePageHorizontalSubView className="credits-section">
      <div class="team">
        <div class="students">
          <h3>INTEGRANTES</h3>
          <div class="students-list">
            <p>
              Nelson Camilo Plata Patiño<br />
              <strong>Email:</strong> nplata2@udi.edu.co
            </p>
            <p>
              Jesús David Felizola Sánchez<br />
              <strong>Email:</strong> jfelizola3@udi.edu.co
            </p>
          </div>
        </div>

        <div class="professors">
          <h3>DIRECTORA DE PROYECTO DE GRADO</h3>
          <div class="professors-list">
            <p>
              Liliana Cortés Garzón<br />
              <strong>Email:</strong> lcortesgarzon@gmail.com
            </p>
          </div>
        </div>
      </div>

      <div class="udi-logo">
        <img
          src="/img/logo-udi.png"
          alt="UDI - Universidad de Investigación y Desarrollo"
        />
      </div>
    </OnePageHorizontalSubView>
  </OnePageView>

  <!-- Second section: cathegories and interviews -->
  <OnePageView>
    <OnePageHorizontalSubView>Here we</OnePageHorizontalSubView>
    <OnePageHorizontalSubView>are</OnePageHorizontalSubView>
  </OnePageView>
</main>

<style>
  main {
    height: 100vh;
  }

  article {
    width: 60%;
    height: 100%;
    font-family: sans-serif;
    color: #333;
    display: flex;
    flex-direction: column;
    justify-content: center;
  }

  h2 {
    font-size: 2rem;
    text-transform: uppercase;
    font-weight: 500;
  }

  p {
    font-size: 1.1rem;
    font-weight: 300;
    line-height: 1.6;
  }

  figure {
    width: 40%;
    height: 100%;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    gap: 1rem;
  }

  figure img {
    width: 55%;
    height: auto;
    display: block;
  }

  figcaption {
    font-size: 0.75rem;
    font-family: sans-serif;
    font-weight: 300;
    text-align: center;
    color: #444;
  }

  .team {
    font-family: sans-serif;
    color: #333;
    display: flex;
    flex-direction: row;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    text-align: center;
    height: 100%;
    width: 60%;
  }

  .team h3 {
    font-size: 1rem;
    font-weight: 700;
    text-transform: uppercase;
  }

  .team p {
    font-size: 0.95rem;
    line-height: 1.5;
  }

  .udi-logo {
    flex-shrink: 0;
    display: flex;
    justify-content: center;
    align-items: center;
    width: 40%;
    height: 100%;
  }

  .udi-logo img {
    width: 160px;
    height: auto;
  }

  .students-list,
  .professors-list {
    display: flex;
    flex-direction: row;
    align-items: center;
    flex-wrap: wrap;
    gap: 6rem;
  }

  .students,
  .professors {
    width: 100%;
    height: 50%;
    display: flex;
    flex-direction: column;
    justify-content: left;
  }

  .students h3,
  .professors h3 {
    font-weight: 700;
    text-align: left;
    text-transform: uppercase;
  }

  .students-list p,
  .professors-list p {
    font-size: 0.95rem;
    line-height: 1.5;
    text-align: left;
  }
</style>
