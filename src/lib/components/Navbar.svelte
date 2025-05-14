<script>
  import { goto } from '$app/navigation';
</script>

<nav>
  <img src="/logo-bucaramanga.png" alt="Archivo Fotográfico de Bucaramanga" class="logo" />
  <div class="nav-links">
    <button on:click={() => goto('/#categories')}>ARCHIVO</button>
    <button on:click={() => goto('/authors')}>AUTORES</button>
  </div>
</nav>

<style>
  nav {
    position: absolute;
    top: 1.5rem;
    left: 2rem;
    right: 2rem;
    display: flex;
    justify-content: space-between;
    align-items: center;
    z-index: 20;
  }

  .logo {
    height: 88px;
    width: auto;
  }

  .nav-links {
    display: flex;
    gap: 2rem;
    padding-right: 1rem;
  }

  .nav-links button {
    background: none;
    border: none;
    color: white;
    font-family: sans-serif;
    font-weight: 300;
    font-size: 0.9rem;
    cursor: pointer;
  }

  .nav-links button:hover {
    border-bottom: 1px solid white;
  }
</style>
