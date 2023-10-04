<script lang="ts">
  import { base } from "$app/paths";
  import DbContents from "$lib/components/DbContents.svelte";
</script>

<style>
  nav {
    max-width: 40rem;
    margin: auto;
    padding: 1rem;
    display: flex;
    gap: 1rem;
  }

  main {
    max-width: 40rem;
    margin: auto;
    padding: 0 1rem;
  }

  main > *:not(:last-child) {
    margin-bottom: 1rem;
  }

  :global(img) {
    max-width: 100%;
  }
</style>

<nav>
  <a href="{base}/">Home</a>
  <a href="{base}/about">About</a>
</nav>

<DbContents />
<main>
  <slot />
</main>
