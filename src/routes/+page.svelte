<script lang="ts">
  let userName = $state("Existing Username");
  $inspect(userName);
</script>

<h1>Your userName</h1>
<input type="text" bind:value={userName} />

<p>{userName}</p>

<style>
  h1 {
    color: rgb(86, 86, 189);
    font-family: Arial, Helvetica, sans-serif;
  }

  /* .container {
    display: flex;
    justify-content: space-between;
  } */
</style>
