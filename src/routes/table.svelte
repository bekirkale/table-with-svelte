<script>
    import Column from './column.svelte'
    export let r=[];//for rows
    export let c=[];//for columns
</script>

<table>
    <thead>
        <tr>
            {#each {length:c} as column}
            <th contenteditable ></th>
            {/each}
        </tr>
    </thead>
    <tbody>
    {#each {length:r} as row}
        <tr>
            {#each {length:c} as column}
                <Column  />
            {/each}
        </tr>
    {/each}
</tbody>	
</table>

<style>
    table {
        border:black 1px solid;
        border-collapse:collapse;
    }
</style>