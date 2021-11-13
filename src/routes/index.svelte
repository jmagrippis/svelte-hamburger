<script context="module" lang="ts">
  export const prerender = true
</script>

<script lang="ts">
  import Hamburger from '$lib/Hamburger.svelte'
</script>

<svelte:head>
  <title>Hamburger</title>
</svelte:head>

<section>
  <Hamburger width={500} />
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
