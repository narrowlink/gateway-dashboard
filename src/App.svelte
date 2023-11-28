<script lang="ts">
  import init, { greet } from "types-wrapper";
  import Test from "./lib/Test.svelte";

  init().then(() => {
    console.log("init wasm-pack");
    // greet("from vite!");
  });
</script>

<h1 class="text-3xl font-bold underline">Hello world!</h1>
<Test />

<style lang="postcss">
  :global(html) {
    background-color: theme(colors.gray.100);
  }
</style>
