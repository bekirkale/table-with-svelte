<script>
import Tablecreator from './table-creator.svelte'
import Qa from './qa.svelte'
	let activeProject=""
</script>
<p>PROJECTS:</p>
<div id="project-names" >
	<button on:click={() => activeProject="table-creator" }>Table Creator</button>
	<button on:click={ () => activeProject="QAs"}>QAs</button>
</div>

<div>::::::::::</div>

<div id="projects">
	{#if activeProject=="table-creator"}
		<Tablecreator />
	{:else if activeProject=="QAs"}
		<Qa />
	{/if}
</div>

