<script lang="ts">
  let showDropdown: boolean = false

  function toggleDropdown() {
    showDropdown = !showDropdown
  }
</script>

<li>
  <!-- svelte-ignore a11y-click-events-have-key-events -->
  <!-- svelte-ignore a11y-missing-attribute -->
  <a class="has-icon has-dropdown-icon" 
    on:click={toggleDropdown} 
    role="button" 
    tabindex="-1" 
    href="/components/forms"
  >
    <span class="icon">
      <span class="material-icons-sharp is-size-6">dynamic_form</span>
    </span>
    <span class="menu-item-label">Forms</span>
    <!-- dropdown -->
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
  <ul class="flat">
    <li>
      <a href="/components/forms">
        <span>All</span>
      </a>
    </li>
    <li>
      <a href="/components/forms/buttons">
        <span>Buttons</span>
      </a>
    </li>
    <li>
      <a href="/components/forms/check-radio">
        <span>Checkbox/Radio</span>
      </a>
    </li>
    <li>
      <a href="/components/forms/input">
        <span>Input Fields</span>
      </a>
    </li>
    <li>
      <a href="/components/forms/sample">
        <span>Sample Form</span>
      </a>
    </li>
    <li>
      <a href="/components/forms/select">
        <span>Select</span>
      </a>
    </li>
    <li>
      <a href="/components/forms/textarea">
        <span>Textarea</span>
      </a>
    </li>
  </ul>
  {/if}        
</li>