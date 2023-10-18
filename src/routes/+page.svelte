<script>
import Tablecreator from './table-creator.svelte'
let activeProject=""

</script>


<div id="project-names" >
	<button on:click={ () = > activeProject="table-creator" }>Table Creator</button>
</div>

<div id="projects">
	{#if activeProject=="table-creator"}
	<Tablecreator />
	{/if}
</div>