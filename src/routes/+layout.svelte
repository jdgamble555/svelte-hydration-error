<script lang="ts">
  import { browser } from "$app/environment";
  import "../app.css";
  let { children } = $props();

  const markup = `<div ${browser ? "light" : "dark"}></div>`;
</script>

{@render children()}

<svelte:head>
  <!-- svelte-ignore hydration_html_changed hydration_mismatch -->
  {@html markup}
</svelte:head>
