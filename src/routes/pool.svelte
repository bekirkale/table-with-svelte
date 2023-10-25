<script>
    let options=[]
    let renderList
    let value
   
    function addOption(event){
        if(event.keyCode==13){
            options.push(value)
            options=options
            value=""         
        }
    }
</script>

    <p>The Pool:</p>

    <input type="text" bind:value on:keyup={addOption}>
   
    {#each options as option}
        <p><input bind:value={option}></p> 
    {/each}
  
    <button on:click={ () => {renderList=options.slice(); renderList=renderList}}>Render</button>

    {#if renderList}
        <p>{renderList[0]}</p>
        {#each renderList.slice(1) as radio  }
            <div>
                <input type="radio" value={radio} >
                <label for={radio}>{radio}</label>
            </div>   
        {/each}
        
    {/if}
