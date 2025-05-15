<script>
  import Carousel from "$lib/components/Carousel.svelte";
  import Navbar from "$lib/components/Navbar.svelte";
</script>

<header>
  <Navbar />
  <Carousel />
</header>

<main>
  <section class="page">
    <!-- Text + Image -->
    <div class="content">
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
    </div>

    <!-- Credits + Logo -->
    <div class="credits-section">
      <div class="team">
        <h3>INTEGRANTES</h3>
        <p>
          Nelson Camilo Plata Patiño<br />
          <strong>Email:</strong> nplata2@udi.edu.co
        </p>
        <p>
          Jesús David Felizola Sánchez<br />
          <strong>Email:</strong> jfelizola3@udi.edu.co
        </p>

        <h3>DIRECTORA DE PROYECTO DE GRADO</h3>
        <p>
          Liliana Cortés Garzón<br />
          <strong>Email:</strong> lcortesgarzon@gmail.com
        </p>
      </div>

      <div class="udi-logo">
        <img
          src="/img/logo-udi.png"
          alt="UDI - Universidad de Investigación y Desarrollo"
        />
      </div>
    </div>
  </section>
</main>

<style>
  main {
    height: 100vh;
  }

  .page {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    height: 100vh;
  }

  .content {
    display: flex;
    flex-wrap: wrap;
    max-width: 1200px;
    margin: 3rem auto;
    padding: 0 2rem;
    gap: 2rem;
    height: 50%;
    align-items: center;
    justify-content: center;
  }

  article {
    flex: 1 1 60%;
    font-family: sans-serif;
    color: #333;
  }

  h2 {
    font-size: 1.8rem;
    text-transform: uppercase;
    font-weight: 700;
    margin-bottom: 1rem;
  }

  p {
    font-size: 1.4rem;
    font-weight: 300;
    line-height: 1.6;
  }

  figure {
    flex: 1 1 30%;
    margin: 0;
  }

  figure img {
    width: 100%;
    height: auto;
    display: block;
  }

  figcaption {
    font-size: 0.75rem;
    font-family: sans-serif;
    font-weight: 300;
    text-align: center;
    color: #444;
    margin-top: 0.5rem;
  }

  .credits-section {
    display: flex;
    justify-content: space-between;
    align-items: flex-start;
    margin: 3rem auto;
    padding: 0 2rem;
    border-top: 1px solid #ccc;
    gap: 2rem;
    flex-wrap: wrap;
    background-color: #efeded;
    height: 50%;
  }

  .team {
    flex: 1;
    font-family: sans-serif;
  }

  .team h3 {
    font-size: 1rem;
    margin-bottom: 0.5rem;
    font-weight: 700;
    text-transform: uppercase;
  }

  .team p {
    font-size: 0.95rem;
    line-height: 1.5;
    margin-bottom: 1rem;
  }

  .udi-logo {
    flex-shrink: 0;
  }

  .udi-logo img {
    width: 160px;
    height: auto;
  }
</style>
