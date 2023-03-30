<script>
  export let player;

  console.log(player)

</script>

<article class="card">
  <a href={player.link} target="_blank"> 
    <h3>{player.title}</h3>
    <img class="player" src="/{player.images}" width="300" height="300" alt="player images" />
    <img class="teamLogo" src="/arsenal-logo.svg" alt='arsenal logo'/>
    <h3>{player.id}</h3>
    <h3>{player.position}</h3>
    <p>{player.description}</p>
    <p>{player.link}</p>
   </a> 
</article>



<style>

  .teamLogo{
    width:100px;
    margin:0 auto;
  }


  article {
    width: 100%;
    margin: 0;
    border-radius: 1px rgb(8, 8, 8);
    justify-content: center;
    box-shadow: 0 2px 2px rgb(179, 10, 10);
    align-items: flex-start;
  }
  article :hover {
    background-color: rgb(179, 10, 10);
    color: rgb(255, 255, 255);
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
    margin: 0 auto;
    grid-gap: 2em;
  }

  @media (min-width: 80em) {
    .card {
      display: flex;
      justify-content: center;
      align-items: center;
      width:420px;
      grid-template-columns: repeat(3, 1fr);
      margin: 0;
    }
  }
</style>