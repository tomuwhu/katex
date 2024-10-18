<script>
  import katex from 'katex'
  import { onMount } from 'svelte';
  var input = "\\sqrt[3]{\\frac{2^7-2^x}{2^x-2}}=2"
  $:kt = katex.renderToString(input, {output: 'mathml'})
</script>

<main>
  <input type="text" bind:value={input}>
  <hr>
  <div>
    {@html kt}
  </div>
</main>

<style>
input {
  font-size: 30px;
  width: 700px; 
}
:global(.katex) {
  font-size: 60px;
}
</style>
