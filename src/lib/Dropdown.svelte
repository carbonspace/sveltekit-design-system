<script lang="ts">
  export let showDropdown: boolean = false
  // let dropdown

  export function toggleDropdown() {
    showDropdown = !showDropdown
  }
</script>

<button on:click>A button</button>