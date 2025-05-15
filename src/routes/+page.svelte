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

  <!-- Second section: categories and interviews -->
  <OnePageView>
    <OnePageHorizontalSubView className="categories-section">
      <div class="categories-container">
        <div class="title">
          <h2>CATEGORÍAS</h2>
        </div>
        <div class="categories-list">
          <div class="category">
            <div class="category-image">
              <img src="/img/urbanismo.avif" alt="Urbanismo" />
            </div>
            <h3>Urbanismo</h3>
            <p>
              Explora la colección de fotografías urbanas, un testimonio visual
              de la evolución de la planificación y estructural de la ciudad.
              Descubre cómo cada imagen revela el impacto del urbanismo en el
              entorno.
            </p>
          </div>

          <div class="category">
            <div class="category-image">
              <img src="/img/arquitectura.avif" alt="Arquitectura" />
            </div>
            <h3>Arquitectura</h3>
            <p>
              Sumérgete en nuestra colección de fotografías arquitectónicas,
              donde cada imagen captura la transformación y los estilos que han
              definido el paisaje urbano bumangués.
            </p>
          </div>

          <div class="category">
            <div class="category-image">
              <img src="/img/vida-cotidiana.avif" alt="Vida cotidiana" />
            </div>
            <h3>Vida cotidiana</h3>
            <p>
              Donde cada imagen cuenta historias de personas, momentos y
              tradiciones que dan forma al alma de la ciudad.
            </p>
          </div>
        </div>
      </div>
    </OnePageHorizontalSubView>
    <OnePageHorizontalSubView className="fifty-fifty-2"
    ></OnePageHorizontalSubView>
  </OnePageView>
</main>

<style>
  main {
    height: 100vh;
  }

  .category-image {
    display: flex;
    justify-content: center;
    align-items: center;
    width: 100%;
    height: 70%;
  }

  .category-image > img {
    width: 40%;
    display: block;
  }

  .category > p {
    font-size: 1rem;
    font-weight: 300;
    text-align: center;
  }

  .title {
    font-family: sans-serif;
    color: #333;
    display: flex;
    justify-content: center;
    align-items: center;
    text-align: center;
    height: 20%;
    justify-content: flex-start;
  }

  .title h2 {
    font-size: 2rem;
    text-transform: uppercase;
    font-weight: 500;
  }

  .categories-list {
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: center;
    gap: 8rem;
    height: 80%;
  }

  .category {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    height: 100%;
  }

  .categories-container {
    display: flex;
    flex-direction: column;
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
    justify-content: flex-start;
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

  .categories-container {
    display: flex;
    flex-direction: column;
    height: 100%;
    width: 100%;
    padding: 2rem;
    box-sizing: border-box;
  }

  .title {
    text-align: left;
    margin-bottom: 2rem;
  }

  .title h2 {
    font-size: 2rem;
    text-transform: uppercase;
    font-weight: 600;
  }

  .categories-list {
    display: flex;
    justify-content: space-around;
    align-items: flex-start;
    gap: 2rem;
    flex-wrap: wrap;
    height: 100%;
  }

  .category {
    flex: 1 1 250px;
    max-width: 300px;
    display: flex;
    flex-direction: column;
    align-items: center;
    text-align: center;
  }

  .category-image {
    width: 100%;
    aspect-ratio: 4/3;
    overflow: hidden;
    display: flex;
    justify-content: center;
    align-items: center;
    margin-bottom: 1rem;
  }

  .category-image img {
    width: 100%;
    height: 100%;
    object-fit: cover;
    display: block;
  }

  .category h3 {
    font-size: 1.2rem;
    text-transform: uppercase;
    margin: 0.5rem 0;
  }

  .category p {
    font-size: 0.95rem;
    font-weight: 300;
    line-height: 1.4;
  }

  .categories-container {
    display: flex;
    flex-direction: column;
    flex: 1;
    overflow: hidden;
  }

  .title {
    height: 20%;
    display: flex;
    align-items: center;
    padding-left: 1rem;
  }

  .title h2 {
    font-size: 1.8rem;
    text-transform: uppercase;
    font-weight: 600;
    margin: 0;
  }

  .categories-list {
    height: 80%;
    display: flex;
    justify-content: space-around;
    align-items: stretch;
    gap: 2rem;
    padding: 0 1rem;
    overflow: hidden;
  }

  .category {
    flex: 1;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: flex-start;
    padding: 1rem;
    box-sizing: border-box;
    overflow: hidden;
  }

  .category-image {
    width: 100%;
    height: 60%;
    display: flex;
    justify-content: center;
    align-items: center;
    overflow: hidden;
  }

  .category-image img {
    width: 100%;
    height: 100%;
    object-fit: cover;
  }

  .category h3 {
    font-size: 1.2rem;
    margin: 0.5rem 0 0;
    text-transform: uppercase;
    font-weight: 600;
  }

  .category {
    margin: 0;
    padding: 0.5rem;
  }

  .categories-container {
    display: flex;
    flex-direction: column;
    flex: 1;
    overflow: hidden;
  }

  .title {
    height: 20%;
    display: flex;
    align-items: center;
    margin: 0;
  }

  .title h2 {
    margin: 0;
    font-size: 1.8rem;
    text-transform: uppercase;
    font-weight: 600;
  }

  .categories-list {
    height: 80%;
    display: flex;
    justify-content: space-around;
    align-items: center;
    padding: 0;
    margin: 0;
  }

  .category {
    flex: 1;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: start;
    box-sizing: border-box;
    overflow: hidden;
    text-align: center;
  }

  .category-image {
    width: 140px;
    height: 140px;
    border-radius: 50%;
    overflow: hidden;
    margin-bottom: 0.5rem;
    border: 3px solid white;
  }

  .category-image {
    width: 160px;
    height: 160px;
    border-radius: 50%;
    overflow: hidden;
    border: 4px solid #444;
  }

  .category-image img {
    width: 100%;
    height: 100%;
    object-fit: cover;
  }

  .category h3 {
    font-size: 1.2rem;
    font-weight: 600;
    text-transform: uppercase;
  }

  .category p {
    font-size: 0.95rem;
    font-weight: 300;
    line-height: 1.4;
    margin: 0;
  }
</style>
