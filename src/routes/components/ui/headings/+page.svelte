<script>
	import Headings from "$lib/patterns/ui/Headings.svelte";
</script>

<svelte:head>
	<title>Headings</title>
	<meta name="description" content="About this app" />
</svelte:head>

<section class="hero is-hero-bar">
  <div class="hero-body">
    <div class="level">
      <div class="level-left">
        <div class="level-item">
          <h1 class="title">Headings</h1>
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
</section>