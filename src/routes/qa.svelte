<script>
    import InputBox from './inputBox.svelte'
    let toggle = false
    let list = []
    let item =[]
    let i = 1
    
    function BoxDone(event){
       if(toggle == false){
        item.push({q: event.detail.text})
       }else{
        item.push({a: event.detail.text})
       }
       if(item.length==2){
        list.push(item)
        item =[]
       }
        list = list
        toggle = !toggle
    }

</script>
   
    {#if toggle == false }
        <InputBox kind = "q" on:done={BoxDone} />
    {:else if toggle == true}
        <InputBox kind = "a" on:done={BoxDone} />
    {/if}


    {#each list as QAs, i}
        <p>{i+1}.</p>
        <p>Q:{JSON.stringify(QAs[0].q)}</p>
        <p>A:{JSON.stringify(QAs[1].a)}</p>
    {/each}

