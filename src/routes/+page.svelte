<script>
	import Table from './table.svelte'
	let row
	let column
</script>

<input type="number" min=0 bind:value={row}>
<input type="number" min=0 bind:value={column}>

{#if row>0 && column>0}
	<Table r={row} c={column}/>
{/if}


