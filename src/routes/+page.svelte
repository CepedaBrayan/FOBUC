<script>
  import Carousel from "$lib/components/Carousel.svelte";
  import InterviewContainer from "$lib/components/InterviewContainer.svelte";
  import MoreThan100Photos from "$lib/components/MoreThan100Photos.svelte";
  import Navbar from "$lib/components/Navbar.svelte";
  import OnePageHorizontalSubView from "$lib/components/OnePageHorizontalSubView.svelte";
  import OnePageView from "$lib/components/OnePageView.svelte";
  import { photos } from "$lib/data/moreThan100Photos";
</script>

<main>
  <OnePageView>
    <div class="carousel-wrapper">
      <Navbar />
      <Carousel />
    </div>
  </OnePageView>

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

  <!-- Second section: categories -->
  <OnePageView>
    <OnePageHorizontalSubView className="categories-section">
      <div class="categories-container">
        <div class="title">
          <h2>CATEGORÍAS</h2>
        </div>
        <div class="categories-list">
          <div class="category category-left-side">
            <div class="category-image">
              <img src="/img/urbanismo.avif" alt="Urbanismo" />
            </div>
            <div class="category-text">
              <h3>Urbanismo</h3>
              <p>
                Explora la colección de fotografías urbanas, un testimonio
                visual de la evolución de la planificación y estructural de la
                ciudad. Descubre cómo cada imagen revela el impacto del
                urbanismo en el entorno.
              </p>
            </div>
            <div class="category-ver-mas">
              <p>
                <a href="/urbanismo">Ver más</a>
              </p>
            </div>
          </div>

          <div class="category">
            <div class="category-image">
              <img src="/img/arquitectura.avif" alt="Arquitectura" />
            </div>
            <div class="category-text">
              <h3>Arquitectura</h3>
              <p>
                Sumérgete en nuestra colección de fotografías arquitectónicas,
                donde cada imagen captura la transformación y los estilos que
                han definido el paisaje urbano bumangués.
              </p>
            </div>
            <div class="category-ver-mas">
              <p>
                <a href="/arquitectura">Ver más</a>
              </p>
            </div>
          </div>

          <div class="category category-right-side">
            <div class="category-image">
              <img src="/img/vida-cotidiana.avif" alt="Vida cotidiana" />
            </div>
            <div class="category-text">
              <h3>Vida cotidiana</h3>
              <p>
                Donde cada imagen cuenta historias de personas, momentos y
                tradiciones que dan forma al alma de la ciudad.
              </p>
            </div>
            <div class="category-ver-mas">
              <p>
                <a href="/vida-cotidiana">Ver más</a>
              </p>
            </div>
          </div>
        </div>
      </div>
    </OnePageHorizontalSubView>
  </OnePageView>

  <!-- Third section: interviews -->
  <OnePageView>
    <OnePageHorizontalSubView className="interviews-section"
      ><InterviewContainer
        image="/img/entrevista1.avif"
        title="Gavassa"
        subtitle="El Legado de Gavassa"
      /></OnePageHorizontalSubView
    >
    <OnePageHorizontalSubView className="interviews-section"
      ><InterviewContainer
        image="/img/entrevista2.avif"
        title="Gerardo Arenas"
        subtitle="Gerardo Arenas"
      /></OnePageHorizontalSubView
    >
    <OnePageHorizontalSubView className="interviews-section"
      ><InterviewContainer
        image="/img/entrevista3.avif"
        title="Natalia Pinilla"
        subtitle="Natalia Pinilla"
      /></OnePageHorizontalSubView
    >
  </OnePageView>

  <!-- Fourth section: more than 100 photos -->
  <OnePageView>
    <OnePageHorizontalSubView className="more-than-photos-section">
      <MoreThan100Photos {photos} />
    </OnePageHorizontalSubView>
  </OnePageView>

  <!-- Fifth section: footer -->
  <OnePageView>
    <OnePageHorizontalSubView className="footer-section">
      <div class="footer-container">
        <div class="footer-logo">
          <img
            src="/logo-bucaramanga-negro.png"
            alt="Fototeca de Bucaramanga"
          />
        </div>

        <div class="footer-contacts">
          <h3>Investigadores</h3>
          <div class="footer-researchers">
            <p>
              Nelson Camilo Plata Patiño<br />
              <strong>Email:</strong> nplata2@udi.edu.co
            </p>
            <p>
              Jesús David Felizola Sánchez<br />
              <strong>Email:</strong> jfelizola3@udi.edu.co
            </p>
          </div>

          <h3>Directora de Proyecto de grado</h3>
          <p>
            Liliana Cortés Garzón<br />
            <strong>Email:</strong> lcortesgarzon@gmail.com
          </p>
        </div>

        <div class="footer-udi">
          <img
            src="/img/logo-udi.png"
            alt="UDI - Universidad de Investigación y Desarrollo"
          />
          <p>Calle 9 No. 23-55 Bucaramanga</p>
          <p><strong>Teléfono:</strong> 6352525 Ext. 134 y 167</p>
          <p><strong>Email:</strong> je.grafico@udi.edu.co</p>
        </div>
      </div>

      <div class="footer-note">
        <p>
          Este sitio web ha sido desarrollado con fines exclusivamente
          académicos y educativos, como parte de un proyecto universitario. No
          tiene ánimo de lucro ni propósito comercial.
        </p>
        <p>
          Todas las imágenes utilizadas en este sitio pertenecen a sus
          respectivos autores y proceden de archivos públicos, colecciones
          institucionales o recursos educativos disponibles en línea. Se han
          incluido únicamente con fines de análisis, documentación y estudio,
          respetando los principios de uso justo (fair use) en contextos
          académicos.
        </p>
        <p>
          Si usted es titular de derechos sobre alguno de los contenidos aquí
          presentados y considera que su uso no es apropiado, por favor
          contáctenos para atender su solicitud.
        </p>
      </div>
    </OnePageHorizontalSubView>
  </OnePageView>
</main>

<style>
  main {
    height: 100vh;
    overflow-y: scroll;
    scroll-snap-type: y mandatory;
    scroll-behavior: smooth;
    scrollbar-width: none; /* Firefox */
    -ms-overflow-style: none; /* IE y Edge */
  }

  .carousel-wrapper {
    position: relative;
    width: 100%;
    height: 100vh;
    overflow: hidden;
    z-index: 1;
  }

  .category-image {
    border-radius: 50%;
    overflow: hidden;
    border: 4px solid #444;
  }

  .category-text {
    display: flex;
    flex-direction: column;
    align-items: center;
    width: 100%;
    height: 40vh;
  }

  .category-ver-mas {
    display: flex;
    justify-content: center;
    align-items: center;
    width: 100%;
    height: 20%;
  }

  .category-text > p {
    font-size: 1.2rem;
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
    text-align: left;
    margin-bottom: 2rem;
    border-bottom: 3px solid #333;
  }

  .title h2 {
    font-size: 2rem;
    text-transform: uppercase;
    font-weight: 500;
  }

  .category-left-side {
    border-right: 3px solid #333;
  }

  .category-right-side {
    border-left: 3px solid #333;
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

  .categories-list {
    height: 80%;
    display: flex;
    justify-content: space-around;
    align-items: center;
    padding: 0;
    margin: 0;
    align-items: flex-start;
    gap: 2rem;
    flex-wrap: wrap;
    height: 100%;
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
    padding: 1rem;
  }

  .category-image > img {
    height: 180px;
    width: 180px;
    object-fit: cover;
    object-position: 60% 40%;
  }

  .category h3 {
    font-size: 1.5rem;
    font-weight: 600;
    text-transform: uppercase;
    margin-bottom: 1.5rem;
  }

  .category p {
    font-size: 1.2rem;
    font-weight: 300;
    line-height: 1.7;
    margin: 0;
  }

  .footer-container {
    padding: 2rem 2rem 1rem 2rem;
    display: flex;
    flex-direction: row;
    height: 50vh;
    width: 100%;
  }

  .footer-contacts,
  .footer-udi {
    flex: 1;
    min-width: 250px;
  }

  .footer-contacts h3 {
    margin-top: 1rem;
    font-size: 1rem;
    font-weight: 700;
    text-transform: uppercase;
  }

  .footer-contacts p,
  .footer-udi p {
    font-size: 0.9rem;
    line-height: 1.6;
  }

  .footer-udi img {
    width: 100%;
  }

  .footer-note {
    font-size: 0.85rem;
    color: #666;
    line-height: 1.6;
    height: 50vh;
  }

  .footer-logo,
  .footer-udi {
    width: 20vh;
    height: 100%;
    display: flex;
    flex-direction: column;
    justify-content: center;
    padding: 0 2rem;
  }

  .footer-contacts {
    width: 60vh;
    height: 100%;
    display: flex;
    flex-direction: column;
    justify-content: center;
    border-left: 3px solid #333;
    border-right: 3px solid #333;
    padding: 0 2rem;
  }

  .footer-researchers {
    display: flex;
    flex-direction: row;
    gap: 2rem;
    justify-content: flex-start;
  }
</style>
