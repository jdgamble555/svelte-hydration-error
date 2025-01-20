<script lang="ts">
  import { browser } from "$app/environment";
  import "../app.css";
  let { children } = $props();

</script>

{@render children()}

<svelte:head>
  <!-- svelte-ignore hydration_html_changed -->
  {@html `<script> ${browser ? "\nconst light = true\;" : "\nconst dark = true\;"}</script>`}
</svelte:head>
