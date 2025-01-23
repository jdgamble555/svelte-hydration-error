<script lang="ts">
  import { browser } from "$app/environment";
  import "../app.css";
  let { children } = $props();
</script>

{@render children()}

<svelte:head>
  <!-- eslint-disable-next-line svelte/no-at-html-tags, prefer-template--><!-- svelte-ignore hydration_html_changed -->
  {@html `<script> ${browser ? "\nconst light = true;" : "\nconst dark = true;"}</script>`}
</svelte:head>
