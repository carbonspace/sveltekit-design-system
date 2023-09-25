<script lang="ts">
  // @ts-nocheck
	import { onMount } from 'svelte'
	import '../app.css'
	import '../css/style.css';
	
	import "@fontsource/material-icons-sharp";

	import Navbar from '$lib/Navbar.svelte';
	import Sidebar from '$lib/Sidebar.svelte';
	import Footer from '$lib/Footer.svelte';
	import data from "$lib/components"

  let showDropdown = false

  function toggleDropdown() {
    showDropdown = !showDropdown
  }

  onMount(() => window.scrollTo(0,0))
</script>

<div id="app">
  <Navbar />
  <Sidebar />

	<main>
		<slot />
	</main>

  <Footer />
</div>

<style>

	/* .app {
		display: flex;
		flex-direction: column;
		min-height: 100vh;
	} */

/* 	main {
		flex: 1;
		display: flex;
		flex-direction: column;
		padding: 1rem;
		width: 100%;
		max-width: 64rem;
		margin: 0 auto;
		box-sizing: border-box;
	}

	footer {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		padding: 12px;
	}

	footer a {
		font-weight: bold;
	}

	@media (min-width: 480px) {
		footer {
			padding: 12px 0;
		}
	} */
</style>
