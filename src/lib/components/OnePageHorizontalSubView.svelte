<script>
  export let className = "";
</script>

<section class="one-page-horizontal-subview {className}">
  <slot />
</section>

<style>
  :root {
    --left-space: 25vh;
  }

  .one-page-horizontal-subview {
    padding-left: var(--left-space);
    box-sizing: border-box;
    display: flex;
    width: 100%;
  }

  .city-and-memory-section {
    height: 65vh;
    flex-direction: row;
  }

  .credits-section {
    background-color: #efeded;
    height: 35vh;
    flex-wrap: wrap;
    align-items: center;
    justify-content: center;
    flex-direction: column;
  }
</style>
