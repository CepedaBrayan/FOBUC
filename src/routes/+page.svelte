<script>
  import Carousel from "$lib/components/Carousel.svelte";
  import Navbar from "$lib/components/Navbar.svelte";
</script>

<header>
  <Navbar />
  <Carousel />
</header>

<main>
  <div class="content">
    <article>
      <h2>CIUDAD Y MEMORIA: FOTOGRAFÍA HISTÓRICA DE BUCARAMANGA</h2>
      <p>
        Este sitio web es el resultado de un proyecto académico desarrollado
        como proyecto de grado por estudiantes universitarios, cuyo propósito es
        investigar, recopilar y difundir fotografías históricas que documentan
        el desarrollo urbano, arquitectónico y social de la ciudad de
        Bucaramanga.
        <br /><br />
        El archivo reúne fotografías provenientes de distintos archivos y colecciones,
        nacionales e internacionales, con el fin de facilitar el acceso visual a
        la memoria de una ciudad en transformación.
        <br /><br />
        Este es un proyecto estrictamente académico, sin fines comerciales ni de
        lucro. Todas las fuentes han sido citadas y se ha procurado e intentado solicitar
        autorización cuando ha sido requerida.
      </p>
    </article>

    <figure>
      <img src="/img/right-lateral.avif" alt="" />
      <figcaption>
        Autor: Autor: Carlos Eslava Florez<br />
        Fuente: Banco de la República, Biblioteca Virtual
      </figcaption>
    </figure>
  </div>
</main>

<style>
  .content {
    display: flex;
    flex-wrap: wrap;
    max-width: 1200px;
    margin: 3rem auto;
    padding: 0 2rem;
    gap: 2rem;
    height: 100vh;
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
</style>
