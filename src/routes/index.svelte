<script context="module" lang="ts">
  import AnimatedHamburger from '$lib/AnimatedHamburger.svelte'

  export const prerender = true
</script>

<svelte:head>
  <title>Svelte Hamburger</title>
</svelte:head>

<section>
  <AnimatedHamburger width="95vw" />
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
