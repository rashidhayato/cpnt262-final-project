
<script>
    import { page } from '$app/stores';
    import { players } from "$lib/player.js";
    import Card from "$lib/card.svelte";
  let getPlayer;


  for (let player of players) {
    if (player.id === $page.params.id) {
      getPlayer = player;
      break;
    }
  
  }
  
</script>

<h1>{$page.params.player}</h1>

<main>
  <article class="card">
    <img
      src="/{getPlayer.images}"
      width="300"
      height="300"
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