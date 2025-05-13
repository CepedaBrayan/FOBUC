<script>
  export let text;
  export let onClick;
</script>

<button on:click={onClick} class="hover-button">{text}</button>

<style>
  .hover-button {
    border: none;
    background: none;
    cursor: pointer;
    position: relative;
  }

  .hover-button::after {
    content: '';
    display: block;
    height: 2px;
    background: black;
    transition: width 0.3s;
    width: 0;
    position: absolute;
    bottom: 0;
    left: 0;
  }

  .hover-button:hover::after {
    width: 100%;
  }
</style>
