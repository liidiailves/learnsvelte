<script>
    let counter = 0;
    let message= 'Hello Svelte';
    let items = ['piim', 'sai', 'viin'];

    // function add(){
    //     alert('asdasd');
    // }
    // modal oleks parem

    function add(){
        items.push(message);
        // vaja väärtuse sättimist:
        items = items; 
        message = '';
    }
</script>

<button class="button is-primary" on:click={() => counter++}>Value is {counter}</button>

<div class="content">
    <!-- kift lahendus! -->
    <input type="text" class="input" bind:value={message}> 
    <button class="button is-primary" on:click={add}>Add</button>
    
    <h1>{message}</h1>
    <ul>
        {#each items as item}
            <li>{item}</li>
            {/each}
    </ul>
</div>
<!-- <style lang="scss">$color: red;
.button {
    color: $color !important;
}</style> -->

