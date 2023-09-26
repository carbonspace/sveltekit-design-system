<script>
  import { page } from "$app/stores"
  $: isActive = $page.url.pathname === $$props.href
</script>

<!-- svelte-ignore a11y-missing-attribute -->
<a {...$$props} class:active={isActive}>
  <slot />
</a>

<style>
  a {
    color: black;
    text-decoration: none;
    padding: 1rem;
  }
  a.active {
    background: lightgray;
  }
</style>