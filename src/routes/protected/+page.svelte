<script>
  import { page } from "$app/stores";
  export let session;
  $: console.log({ data: $page.data });
</script>

<h1>Protected</h1>
<a href="/">public route</a>
