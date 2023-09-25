<script lang="ts">
	import { page } from '$app/stores'

	export let showDropdown: boolean = false;
	export function toggleDropdown() {
    showDropdown = !showDropdown
  }
</script>

<li>
	<a class="has-icon has-dropdown-icon" on:click={toggleDropdown} on:keypress="{() => {}}" role="button" tabindex="-1" href="#!">
		<span class="icon has-update-mark">
			<span class="material-icons-sharp is-size-6">view_list</span>
		</span>
		<span class="menu-item-label">UI Elements</span>
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
				<a href="/components/ui">
					<span>All</span>
				</a>
			</li>
			<li>
				<a
					href="/components/ui/headings"
					class:is-active={$page.url.pathname === '/components/ui/headings'}
				>
					<span>Headings</span>
				</a>
			</li>
			<li>
				<a 
          href="/components/ui/inline" 
          class:is-active={$page.url.pathname === '/components/ui/inline'}
        >
					<span>Inline Elements</span>
				</a>
			</li>
			<li>
				<a 
          href="/components/ui/lists"
          class:is-active={$page.url.pathname === '/components/ui/lists'}
        >
					<span>Lists</span>
				</a>
			</li>
			<li>
				<a 
          href="/components/ui/paragraphs"
          class:is-active={$page.url.pathname === '/components/ui/paragraphs'}
        >
					<span>Paragraphs</span>
				</a>
			</li>
		</ul>
	{/if}
</li>
