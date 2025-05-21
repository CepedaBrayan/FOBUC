<script>
  export let image;
  export let title;
  export let subtitle;
  export let interviewURL;
</script>

<a
  href={interviewURL}
  target="_blank"
  rel="noopener noreferrer"
  class="interview-card"
>
  <div class="interview-text">
    <h2>ENTREVISTA</h2>
    <h3>{subtitle}</h3>
  </div>
  <div class="interview-image">
    <img src={image} alt={title} />
  </div>
</a>

<style>
  .interview-card {
    display: flex;
    background-color: #222;
    padding-left: 2rem;
    color: white;
    margin-bottom: 1.5rem;
    overflow: hidden;
    height: 100%;
    width: 65%;
    text-decoration: none;
  }

  .interview-card:hover {
    cursor: pointer;
    background-color: #333;
  }

  .interview-text {
    display: flex;
    flex-direction: column;
    justify-content: center;
    font-family: "Georgia", serif;
    flex: 1;
  }

  .interview-text h2 {
    font-size: 3rem;
    font-weight: 400;
    text-transform: uppercase;
    margin: 0;
  }

  .interview-text h3 {
    font-size: 2.8rem;
    font-weight: 300;
    font-family: "Great Vibes", cursive;
    margin: 0.5rem 0 0 0;
  }

  .interview-image {
    flex-shrink: 0;
    margin-left: 2rem;
    height: 100%;
    width: 40%;
  }

  .interview-image img {
    width: 100%;
    height: 100%;
    border-radius: 2px;
    object-fit: cover;
    object-position: 50% 30%;
  }
</style>
