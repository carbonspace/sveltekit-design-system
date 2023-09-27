<script lang="ts">
	import { page } from '$app/stores'

  export let showDropdown: boolean = false;
  export function toggleDropdown() {
    showDropdown = !showDropdown
  }
</script>

<li>
  <!-- svelte-ignore a11y-missing-attribute -->
  <!-- svelte-ignore a11y-click-events-have-key-events -->
  <a 
    class="has-icon has-dropdown-icon" 
    role="button" 
    on:click={toggleDropdown} 
    tabindex="0" 
    href="/components/sub"
  >
    <span class="icon">
      <span class="material-icons-sharp is-size-6">view_list</span>
    </span>
    <span class="menu-item-label">Submenus</span>
    <div class="dropdown-icon">
      <span class="icon">
        <span class="material-icons-sharp is-size-6">
          {#if showDropdown}
            remove
          {:else}
            add
          {/if}
        </span>
      </span>
    </div>
  </a>
  {#if showDropdown}
  <ul>
    <li>
      <a href="#void">
        <span>Sub-item One</span>
      </a>
    </li>
    <li>
      <a href="#void">
        <span>Sub-item Two</span>
      </a>
    </li>
  </ul>
  {/if}
</li>