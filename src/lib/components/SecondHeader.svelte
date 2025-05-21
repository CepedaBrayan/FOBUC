<script>
  import { goto } from "$app/navigation";
</script>

<div class="second-header">
  <button class="back-button" on:click={() => goto("/")}>Volver</button>

  <div class="header">
    <img src="/img/second-header.avif" alt="Header" class="header-image" />
    <h1 class="logo">FO<span class="bold-b">B</span>UC</h1>
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

  .logo {
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    font-size: 2.5rem;
    font-weight: bold;
    color: white;
    text-shadow: 1px 1px 4px black;
  }

  .bold-b {
    font-weight: normal;
    font-size: 3rem;
  }
</style>
