<script>
    import { createEventDispatcher } from "svelte";
    const dispatch = createEventDispatcher();
    let data
    export let kind

    function save (event){
        if(event.keyCode==13){
            dispatch('done', {
            text:data,
            })
        }
    }
</script>

    {#if kind =="q"}
        Q:<input type="text" bind:value={data} on:keyup={save} autofocus >
    {:else if kind == "a"}
        A:<input type="text" bind:value={data} on:keyup={save} autofocus >
    {/if}

