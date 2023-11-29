<script lang="ts">
  import init, { greet } from "types-wrapper";
  import Test from "./lib/Test.svelte";
  import Logo from "./assets/logo.svg?raw";
  const LogoEncoded = `data:image/svg+xml,${encodeURIComponent(Logo)}`;

  init().then(() => {
    console.log("init wasm-pack");
    // greet("from vite!");
  });
</script>

<svelte:head>
  <link rel="icon" type="image/svg+xml" href={LogoEncoded} />
</svelte:head>
<h1 class="text-3xl font-bold underline">Hello world!</h1>
<Test />

<style lang="postcss">
  :global(html) {
    background-color: theme(colors.gray.100);
  }
</style>
