<script>
  import UserInput from "$lib/components/UserInput.svelte";

  let data = $props();
  $inspect(data);
</script>

<UserInput userName={"Niklas"}>
  <h1>This is the staff passed inside</h1>
</UserInput>
