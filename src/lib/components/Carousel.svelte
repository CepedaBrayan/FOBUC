<script>
  import { onDestroy, onMount } from "svelte";

  let images = [
    "/img/carousel1.avif",
    "/img/carousel2.avif",
    "/img/carousel3.avif",
    "/img/carousel4.avif",
    "/img/carousel5.avif",
  ];

  let current = 0;
  let interval;
  let isPlaying = true;
  const ms = 8000;
  const next = () => (current = (current + 1) % images.length);

  const togglePlay = () => {
    if (isPlaying) {
      clearInterval(interval);
    } else {
      interval = setInterval(next, ms);
    }
    isPlaying = !isPlaying;
  };

  onMount(() => {
    interval = setInterval(next, ms);
  });

  onDestroy(() => {
    clearInterval(interval);
  });
</script>

<div class="carousel">
  <img src={images[current]} alt="" />
  <div class="overlay">
    <h1>BIENVENIDO AL ARCHIVO FOTOGRÁFICO<br />DE BUCARAMANGA</h1>
    <button class="pause-button" on:click={togglePlay}
      >{isPlaying ? "❚❚" : "▶"}</button
    >
  </div>
</div>

<style>
  .carousel {
    position: relative;
    width: 100%;
    height: 100vh;
    overflow: hidden;
    z-index: 1;
  }

  .carousel img {
    width: 100%;
    height: 100vh;
    object-fit: cover;
    filter: grayscale(100%);
  }

  .overlay {
    position: absolute;
    top: 0;
    left: 0;
    color: white;
    width: 100%;
    height: 100%;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    background: rgba(0, 0, 0, 0.3);
    text-align: center;
    padding: 0 2rem;
  }

  h1 {
    font-size: 4rem;
    font-weight: 500;
    margin-bottom: auto;
    padding-top: 25rem;
  }

  .pause-button {
    position: absolute;
    bottom: 2rem;
    left: 2rem;
    background: rgba(255, 255, 255, 0.4);
    border: none;
    border-radius: 50%;
    width: 32px;
    height: 32px;
    font-size: 1rem;
    cursor: pointer;
  }
</style>
