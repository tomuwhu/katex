<script>
  import katex from 'katex'
  import { onMount } from 'svelte';
  var input = "\\sqrt[3]{\\frac{2^7-2^x}{2^x-2}}=2"
  $:kt = katex.renderToString(input, {output: 'mathml'})
</script>

<main>
  <input type="text" bind:value={input}>
  <div>
    {@html kt}
  </div>
</main>

<style>
:global(.katex) {
  font-size: 60px;
}
</style>
