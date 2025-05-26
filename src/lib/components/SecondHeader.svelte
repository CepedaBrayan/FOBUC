<script>
  import { goto } from "$app/navigation";
  export let backRoute = "/"; // default to home if not provided
</script>

<div class="second-header">
  <button class="back-button" on:click={() => goto(backRoute)}>Volver</button>

  <div class="header">
    <img src="/img/second-header.avif" alt="Header" class="header-image" />
    <img src="/logo-bucaramanga.png" alt="Logo" class="logo-bucaramanga" />
  </div>
</div>

<style>
  .second-header {
    width: 100vw;
    height: 30vh;
    position: relative;
    overflow: hidden;
    z-index: 1;
  }

  .back-button {
    padding: 0.5rem 1rem;
    background-color: #ddd;
    border: none;
    border-radius: 8px;
    cursor: pointer;
    margin-bottom: 1rem;
    width: 100px;
    position: absolute;
    top: 1.5rem;
    left: 4rem;
    right: 2rem;
    align-items: center;
    z-index: 10;
    font-weight: bold;
  }

  .header {
    position: relative;
    width: 100%;
    height: 100%;
    text-align: center;
    position: relative;
    overflow: hidden;
    border-radius: 8px;
    z-index: 1;
    display: flex;
    justify-content: center;
    align-items: center;
  }

  .header-image {
    width: 100%;
    height: 100%;
    object-fit: cover;
    border-radius: 8px;
    zoom: 5;
    filter: blur(1px);
    -webkit-filter: blur(1px);
  }

  .logo-bucaramanga {
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    width: 300px; /* increase size as needed */
    height: auto;
    z-index: 10;
  }
</style>
