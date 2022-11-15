<script>
    let innerWidth = 0
    let innerHeight = 0
    
    $: condition = innerWidth*1.33 <= innerHeight
</script>

<svelte:window bind:innerWidth bind:innerHeight />

<p> Inner Width: {innerWidth} </p>
<p> Inner Height: {innerHeight} </p>
<p> condition: {condition} </p>

<img src="https://svelte.dev/svelte-logo-horizontal.svg" alt=""
         class="image-basic"
         class:image-conditional={condition}
         />

<style>
    .image-basic {
        width: 100vw;
    }
    .image-conditional {
        width: 50vw;
    }

</style>