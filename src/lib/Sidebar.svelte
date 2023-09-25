<script lang="ts">
  import { page } from '$app/stores'
  import { onMount } from 'svelte'
	import Forms from './patterns/forms.svelte';
	import Submenus from './patterns/submenus.svelte';
	import Tables from './patterns/tables.svelte';
	import UserInterface from './patterns/user-interface.svelte';
	import Widgets from './patterns/widgets.svelte';
  import NavLink from './NavLink.svelte'

  onMount(() => window.scrollTo(0,0))

  $: isActive = $page.url.pathname === $$props.href
</script>

<aside class="aside is-placed-left is-expanded">
  <div class="aside-tools">
    <div class="aside-tools-label">
      <span>
        <b>DesignKit</b>
      </span>
    </div>
  </div>
  <div class="menu is-menu-main">

    <p class="menu-label">General</p>
    <ul class="menu-list flat">
      <li>
        <a href="/" class="is-active router-link-active has-icon">            
          <span class="icon">
            <span class="material-icons-sharp is-size-6">language</span>
          </span>
          <span class="menu-item-label">Design Tokens</span>
          <!-- <pre>{JSON.stringify(typeaheadEvents, null, 2)}</pre> -->
        </a>
      </li>
    </ul>

    <p class="menu-label">Patterns</p>
    <ul class="menu-list flat">
      <UserInterface />
      <Forms />
      <Tables />
      <Widgets />
      <Submenus />
    </ul>
    <p class="menu-label">About</p>
    <ul class="menu-list">
      <li>
        <!-- svelte-ignore security-anchor-rel-noreferrer -->
        <a href="https://github.com/" target="_blank" class="has-icon">
          <span class="icon"><i class="mdi mdi-github-circle"></i></span>
          <span class="menu-item-label">GitHub</span>
        </a>
      </li>
      <!-- <li>
        <NavLink href="/about">About</NavLink>

      </li> -->
      <li>
        <!-- svelte-ignore a11y-invalid-attribute -->
        <a href="/about" class="has-icon">
          <span class="icon"><i class="mdi mdi-help-circle"></i></span>
          <span class="menu-item-label">About</span>
        </a>
      </li>
      <li>
        <!-- svelte-ignore a11y-invalid-attribute -->
        <a href="/bulma" class="has-icon">
          <span class="icon"><i class="mdi mdi-help-circle"></i></span>
          <span class="menu-item-label">Bulma</span>
        </a>
      </li>
    </ul>
  </div>
</aside>

<style>
  :global(.active) {
    color: lightblue;
    font-weight: bold;
  }
</style>