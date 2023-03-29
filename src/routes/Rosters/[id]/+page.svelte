
<script>
  import { page } from '$app/stores'
  import { players } from '../players.js';
  import Card from '../Card.svelte';
  let getPlayer;
 
  for (let player of players) {
    if (player.id === $page.params.id) {
      getPlayer = player;
      break;
    }
  
  }
  
</script>


<main>
  <article class="card">
    <img
      src="/{getPlayer.images}"
      width="400"
      height="400"
      alt="player images"
    />

    <a href={getPlayer.url} target="_blank">
      <h3>{getPlayer.title}</h3>
      <p>{getPlayer.description}</p>
    </a>
  </article>
</main>

<style>
  article {
    padding: 1rem;
    display: flex;
    justify-content: center;
    /* gap: 2rem; */
  }
  a {
    margin: 10rem;
    display: block;
    text-decoration: none;
    color: rgb(179, 21, 21);
    border-radius: 1rem;
  }
  a:hover {
    background-color: rgb(200, 214, 214);
    padding: 1rem;
  }
</style>