<script lang="ts">
  let userName = $state("Niklas");

  let isEditMode = $state(false);
  let peopleWaiting = $state(["23fdk3232j", "12324dfdc33"]);
  $inspect(peopleWaiting);
</script>

{#snippet userInput(exampleString: string)}
  <h1>Your userName</h1>
  {#if isEditMode}
    <input type="text" bind:value={userName} />
  {:else}
    <p>{userName}</p>
  {/if}
{/snippet}

{@render userInput("Example 1")}

<button onclick={() => (isEditMode = !isEditMode)}>
  {isEditMode ? "Save changes" : "Edit fields"}
</button>

<button onclick={() => peopleWaiting.push(new Date().getTime().toString())}
  >I'm waiting too!</button
>
