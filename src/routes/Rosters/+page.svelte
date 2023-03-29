<script>
  import {player} from "$lib/players.js";
  import Card from "$lib/card.svelte";
</script>

<main>
  <section>
    {#each player as player}
      <a href="Rosters/{player.id}">
        
        <Card {player} />
      </a>
    {/each}
  </section>
</main>