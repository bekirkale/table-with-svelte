<script>
	import Table from './table.svelte'
	let row
	let column
</script>

    <p>Select Rows and Columns to create a TABLE</p>
    <input type="number" min=0 bind:value={row}>
    <input type="number" min=0 bind:value={column}>

{#if row>0 && column>0}
	<Table r={row} c={column}/>
{/if}
