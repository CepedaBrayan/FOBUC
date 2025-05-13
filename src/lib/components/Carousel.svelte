<script>
  import { onDestroy, onMount } from 'svelte';

  let images = [
    '/img/photo1.jpg',
    '/img/photo2.jpg',
    '/img/photo3.jpg'
  ];

  let current = 0;
  let interval;
  let isPlaying = true;

  const next = () => current = (current + 1) % images.length;

  const togglePlay = () => {
    if (isPlaying) {
      clearInterval(interval);
    } else {
      interval = setInterval(next, 5000);
    }
    isPlaying = !isPlaying;
  };

  onMount(() => {
    interval = setInterval(next, 5000);
  });

  onDestroy(() => {
    clearInterval(interval);
  });
</script>

<div class="carousel">
  <img src={images[current]} alt="" />
  <div class="overlay">
    <h1>BIENVENIDO AL ARCHIVO FOTOGRÁFICO<br>DE BUCARAMANGA</h1>
    <div class="credit">
      Autor: Horst Martin Schutkowski<br>
      Fuente: Staatliche Kunstsammlungen Dresden – Deutsche Fotothek
    </div>
    <button class="pause-button" on:click={togglePlay}>{isPlaying ? '❚❚' : '▶'}</button>
  </div>
</div>

<style>
  .carousel {
    position: relative;
    width: 100%;
    height: 100vh;
    overflow: hidden;
  }

  .carousel img {
    width: 100%;
    height: 100%;
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

  .credit {
    position: absolute;
    bottom: 2rem;
    right: 2rem;
    font-size: 0.7rem;
    font-family: sans-serif;
    color: #ccc;
    text-align: right;
  }

  .pause-button {
    position: absolute;
    bottom: 2rem;
    left: 2rem;
    background: rgba(255,255,255,0.4);
    border: none;
    border-radius: 50%;
    width: 32px;
    height: 32px;
    font-size: 1rem;
    cursor: pointer;
  }
</style>
