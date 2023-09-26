<script>
	import Headings from "$lib/patterns/ui/Headings.svelte";
	import Inline from "$lib/patterns/ui/Inline.svelte";
	import Lists from "$lib/patterns/ui/Lists.svelte";
	import Paragraphs from "$lib/patterns/ui/Paragraphs.svelte";
</script>

<svelte:head>
	<title>UI Elements</title>
	<meta name="description" content="About this app" />
</svelte:head>

<section class="hero is-hero-bar">
  <div class="hero-body">
    <div class="level">
      <div class="level-left">
        <div class="level-item">
          <h1 class="title">UI Elements</h1>
        </div>
      </div>
      <div class="level-right" style="display: none;">
        <div class="level-item" />
      </div>
    </div>
  </div>
</section>

<section class="section is-component-section">
  <Headings />
  <Inline />
  <Lists />
  <Paragraphs />
</section>

<style>
	
</style>