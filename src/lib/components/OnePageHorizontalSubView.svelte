<script>
  export let className = "";
</script>

<section class={"one-page-horizontal-subview " + className}>
  <slot />
</section>

<style>
  :root {
    --left-space: 15vh;
  }

  .one-page-horizontal-subview {
    padding-left: var(--left-space);
    padding-right: var(--left-space);
    box-sizing: border-box;
    display: flex;
    flex-direction: column;
    width: 100%;
    height: 100%; /* ensure it spans the whole parent */
    margin: 0; /* ✅ prevent spacing */
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

  .interviews-section {
    height: 31vh;
    align-items: center;
  }

  .more-than-photos-section {
    height: 100vh;
    display: flex;
    flex-direction: column;
  }

  .categories-section {
    height: 100vh;
    display: flex;
    flex-direction: column;
  }

  .footer-section {
    background-color: #f9f9f9;
    font-family: sans-serif;
    color: #333;
    display: flex;
    flex-direction: column;
    align-items: center;
  }
</style>
