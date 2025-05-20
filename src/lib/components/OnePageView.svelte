<section class="one-page-view">
  <slot />
</section>

<style>
  .one-page-view {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    width: 100%;
    height: 100vh;
    scroll-snap-align: start;
    scroll-snap-stop: always;
  }
</style>
