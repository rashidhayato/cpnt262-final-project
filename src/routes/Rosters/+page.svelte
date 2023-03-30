<script>
  import {players} from "$lib/player.js";
  import Card from "$lib/card.svelte";
  
</script>

<main>
  <section>
    {#each players as player}
      <a href="/Rosters{player.id}">
        <Card {player} />
      </a>
    {/each}
  </section>
</main>