<script>
  export let player;
</script>

<article class="card">
  <!-- <img src="/{player.images}" width="300" height="300" alt="player images" /> -->
  <h3>{player.id}</h3>
  <img src="arsenal-logo" alt='arsenal logo'/>

  <a href={player.title} target="_blank">
    <h3>{player.url}</h3>
    <h3>{player.id}</h3>
    <h3>{player.postion}</h3>
    <p>{player.description}</p>
  </a>
</article>



<style>
  article {
    width: 80%;
    margin: 0;
    border-radius: 1px rgb(8, 8, 8);
    justify-content: center;
    box-shadow: 0 2px 2px rgb(179, 10, 10);
    align-items: flex-start;
  }
  article :hover {
    background-color: rgb(179, 10, 10);
    color: white;
  }
  article img {
    display: block;
    width: 100%;
    object-fit: cover;
  }
  article h3 {
    margin: 0.5rem;
    text-align: center;
  }
  article p {
    text-align: center;
    margin: 2rem;
  }
  .card {
    display: grid;
    margin: 0;
    grid-gap: 2em;
  }
  @media (min-width: 80em) {
    .card {
      grid-template-columns: repeat(3, 1fr);
      margin: 0;
    }
  }
</style>