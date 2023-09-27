<script lang="ts">
  import CardFooter from '$lib/CardFooter.svelte'
  
  let showCardContents = true

  async function toggleCardContents() {
    showCardContents = !showCardContents
  }

  // Lists
  const codeHTML = `<ul>
  <li>One</li>
  <li>Two</li>
  <li>Three</li>
  <li>Four</li>
  <li>Five</li>
</ul>

<ol>
  <li>One</li>  
  <li>Two</li>  
  <li>Three</li>  
  <li>Four</li>  
  <li>Five</li>  
</ol>`
</script>

<!-- Lists -->
<div class="card">
  <header 
    class="card-header" 
    role="button" 
    on:click={toggleCardContents} 
    on:keypress={() => {}} 
    tabindex="0"
  >
    <p class="card-header-title">Lists</p>
    <button
      class="card-header-icon"
      aria-label="more options"
    >
      <span class="icon">
        <span class="material-icons-sharp is-size-4">
          {#if showCardContents}
            expand_more
          {:else}
            expand_less
          {/if}
        </span>
      </span>
    </button>
  </header>

  {#if showCardContents}
  <div class="card-content">
    <div class="content is-flex is-justify-content-space-evenly">
      <span style="width: 200px;">
        <div class="mb-5 has-text-weight-bold">Unordered List</div>
        <ul style="list-style-type: none;">
          <li>One</li>
          <li>Two</li>
          <li>Three</li>
          <li>Four</li>
          <li>Five</li>
        </ul>          
      </span>
      <span style="width: 200px;">
        <div class="mb-5 has-text-weight-bold">Unordered List</div>
        <ul>
          <li>One</li>
          <li>Two</li>
          <li>Three</li>
          <li>Four</li>
          <li>Five</li>
        </ul>          
      </span>
      <span>
        <div class="mb-5 has-text-weight-bold">Ordered List</div>
        <ol>
          <li>One</li>  
          <li>Two</li>  
          <li>Three</li>  
          <li>Four</li>  
          <li>Five</li>  
        </ol>
      </span>
    </div>
  </div>
  
  <CardFooter
    codeHTML={codeHTML}
    codeCSS=""
    codeJS=""
  />
  {/if}
</div>