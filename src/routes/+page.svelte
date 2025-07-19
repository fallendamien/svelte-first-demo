<script lang="ts">
  let username = $state("");

  $effect(() => {
    console.log("$effect rune is initiated");

    if (username) {
      console.log(
        `I will send the name to the database, current username is: ${username}`
      );
    }
  });
</script>

<h1>Your username</h1>
<input type="text" bind:value={username} />

<p>{username}</p>

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
