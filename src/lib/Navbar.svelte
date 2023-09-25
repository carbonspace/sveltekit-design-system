<script>
  // @ts-nocheck
  import Typeahead from "svelte-typeahead"
  import SvelteTooltip from 'svelte-tooltip'

  /**
	 * @type {any}
	 */
   export let data
   let typeaheadEvents = []
  //const extract = (item) => item.pattern
  let e = []
</script>

<nav id="navbar-main" class="navbar is-fixed-top">
  <div class="navbar-brand">
    <a href="#!" class="navbar-item is-hidden-desktop jb-aside-mobile-toggle">
      <span class="icon">
        <!-- <i class="mdi mdi-forwardburger mdi-24px"></i> -->
        <span class="material-icons-sharp is-size-5">menu_open</span>
      </span>
    </a>
    <div class="navbar-item has-control">
      <div class="control is-flex">
        <!-- <input placeholder="Search everywhere..." class="input"> -->
        <!-- <Typeahead
          hideLabel
          label="Search Patterns"
          placeholder={`Search Patterns`}
          {data}
          extract={(item) => item.pattern}
          on:select={({ detail }) => typeaheadEvents = [typeaheadEvents.original.url, detail]}
          on:clear={() => typeaheadEvents = [...typeaheadEvents, "clear"]}                      
        /> -->
        <Typeahead
          focusAfterSelect
          hideLabel
          label="Search Patterns"
          placeholder={`Search Patterns`}            
          {data}
          extract={(item) => item.pattern}
          on:select={(e) => {
            // console.log("select", e.detail.original.url)
            // console.log(e);
            window.location = "http://" + window.location.host + e.detail.original.url
            // document.querySelector('#typeahead-0.mi7fcvgqpto').value=''
          }}
          on:clear={() => typeaheadEvents = [...typeaheadEvents, "clear"]} 
        />
          <div class="tt-wrap">
            <SvelteTooltip tip="ESC to clear; Arrow Up/Down to Choose; ENTER to select" right>
              <span class="material-icons-sharp is-size-5" style="margin-left: 5px; margin-top:10px;cursor: pointer; color: #666;">help_outline</span>
            </SvelteTooltip>              
          </div>
      </div>
    </div>
  </div>
  <div class="navbar-brand is-right">
    <a href="#!" class="navbar-item is-hidden-desktop jb-navbar-menu-toggle" data-target="navbar-menu">
      <span class="icon">
        <i class="mdi mdi-dots-vertical"></i>
        <span class="material-icons-sharp is-size-5">more_vert</span>
      </span>
    </a>
  </div>
</nav>

<style>
  /* Typeahead */
  .tt-wrap {
    color: #fff;
  }
</style>