<script lang="ts">
  import { fly } from 'svelte/transition'

  import AnimatedHamburger from '$lib/AnimatedHamburger.svelte'
  import logo from './svelte-logo.svg'

  export let open = false
  export let onClick = () => {
    open = !open
  }
</script>

<header>
  <div class="main">
    <div class="logo">
      <a href="https://kit.svelte.dev">
        <img src={logo} alt="SvelteKit" />
      </a>
    </div>
    <AnimatedHamburger {open} {onClick} />
  </div>

  {#if open}
    <nav transition:fly={{ y: -200, duration: 400 }}>
      <a href="https://magrippis.com/tube">Videos</a>
      <a href="https://magrippis.com/blog">Blogposts</a>
      <a href="https://magrippis.com/tube">Guides</a>
      <a href="https://magrippis.com/tube">Portfolio</a>
      <a href="https://magrippis.com/milestones">Milestones</a>
    </nav>
  {/if}
</header>

<style>
  header {
    position: relative;
    font-size: 2rem;
    color: var(--accent-color);
    background-color: var(--white);
    z-index: 2;
  }

  .main {
    display: flex;
    justify-content: space-between;
  }

  .logo {
    width: 3em;
    height: 3em;
  }

  .logo a {
    display: flex;
    align-items: center;
    justify-content: center;
    width: 100%;
    height: 100%;
  }

  .logo img {
    width: 2em;
    height: 2em;
    object-fit: contain;
  }

  nav {
    position: absolute;
    z-index: -1;
    width: 100%;
    padding: 1rem;
    display: flex;
    flex-direction: column;
    gap: 0.5rem;
    align-items: center;
    background-color: var(--white);
  }
</style>
