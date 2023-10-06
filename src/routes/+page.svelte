<script lang="ts">
  import { page } from "$app/stores";

  $: userName = $page.data?.session?.user?.name;
</script>

{#if userName}
  <p> Hello {userName} </p>
  <a href="/protected">protected route</a>
  <a href="/auth/signout">sign out</a>
{:else}
  <a href="/auth/signin">sign in</a>
{/if}
