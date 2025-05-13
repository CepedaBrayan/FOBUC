<script>
  import authors from '$lib/data/authors.json';
</script>

<style>
  .author-list {
    padding: 2rem;
  }

  .author-card {
    margin-bottom: 1rem;
    padding: 1rem;
    border: 1px solid #ccc;
  }

  .author-name {
    font-size: 1.3rem;
    font-weight: bold;
  }

  .author-bio {
    margin-top: 0.5rem;
  }
</style>

<section class="author-list">
  {#each authors as author}
    <div class="author-card">
      <div class="author-name">{author.name}</div>
      <div class="author-bio">{author.bio}</div>
    </div>
  {/each}
</section>
