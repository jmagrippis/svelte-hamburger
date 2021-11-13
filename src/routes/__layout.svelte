<script lang="ts">
  import 'modern-normalize/modern-normalize.css'

  import Header from '$lib/header/Header.svelte'
  import '../app.css'
</script>

<Header />

<main>
  <slot />
</main>

<footer>
  <a href="https://magrippis.com/tube">magrippis.com/tube</a>
  <p>🧑‍💻 ^ More tutorials from Johnny ^ 👩‍💻</p>
</footer>

<style>
  main {
    flex: 1;
    display: flex;
    flex-direction: column;
    padding: 1rem;
    width: 100%;
    max-width: 1024px;
    margin: 0 auto;
    box-sizing: border-box;
  }

  footer {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    padding: 40px;
  }

  @media (min-width: 480px) {
    footer {
      padding: 40px 0;
    }
  }
</style>
