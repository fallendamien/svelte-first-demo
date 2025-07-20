<script lang="ts">
  let peopleWaiting = $state(["23fdk3232j", "12324dfdc33"]);
  $inspect(peopleWaiting);
</script>

<h1>Waiting queue</h1>
{#snippet userInput(personId: string)}
  <li>ID for person waiting: {personId}</li>
{/snippet}

<ul>
  {#each peopleWaiting as person}
    {@render userInput(person)}
  {/each}
</ul>

<button onclick={() => peopleWaiting.push(new Date().getTime().toString())}
  >I'm waiting too!</button
>
