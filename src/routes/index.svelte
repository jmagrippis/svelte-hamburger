<script context="module" lang="ts">
  export const prerender = true
</script>

<svelte:head>
  <title>Svelte Hamburger</title>
</svelte:head>

<section>
  <slot />
</section>

<style>
  section {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    flex: 1;
  }
</style>
