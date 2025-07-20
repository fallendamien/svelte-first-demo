<script lang="ts">
  import type { Snippet } from "svelte";

  interface UserInputInterface {
    children: Snippet;
    userName: string;
  }

  let { userName, children, ...props }: UserInputInterface = $props();
</script>

<h1>Your userName</h1>
<input type="text" bind:value={userName} />
{@render children()}

<p>{userName}</p>

<style>
  h1 {
    color: rgb(86, 86, 189);
    font-family: Arial, Helvetica, sans-serif;
  }
</style>
