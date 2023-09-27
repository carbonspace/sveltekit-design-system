<script>
	import Selects from "$lib/patterns/forms/Selects.svelte";
import Buttons from "$lib/patterns/forms/Buttons.svelte";
	import Checkboxes from "$lib/patterns/forms/Checkboxes.svelte";
	import Form from "$lib/patterns/forms/Form.svelte";
	import Inputs from "$lib/patterns/forms/Inputs.svelte";
	import Sliders from "$lib/patterns/forms/Sliders.svelte";
	import TextAreas from "$lib/patterns/forms/TextAreas.svelte";
</script>

<svelte:head>
	<title>Form Elements</title>
	<meta name="description" content="About this app" />
</svelte:head>

<section class="hero is-hero-bar">
  <div class="hero-body">
    <div class="level">
      <div class="level-left">
        <div class="level-item">
          <h1 class="title">Form Elements</h1>
        </div>
      </div>
      <div class="level-right" style="display: none;">
        <div class="level-item" />
      </div>
    </div>
  </div>
</section>

<section class="section is-component-section">
  <Buttons />
  <Checkboxes />
  <Form />
  <Inputs />
  <Selects />
  <Sliders />
  <TextAreas />
</section>

<style>
	
</style>