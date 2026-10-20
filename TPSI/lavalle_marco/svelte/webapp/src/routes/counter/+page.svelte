<script>
    import Counter from "../../lib/components/counter.svelte";
    import DoubleCounter from "../../lib/components/DoubleCounter.svelte";
    let contatore = 0;
    let doppio_contatore = 0;
</script>


<h2>Pagina Counter</h2>


{#if contatore < 5}
    <h2 class="rosso">Il valore del contatore vale: {contatore}</h2>
{:else}
    <h2 class="verde">Il valore del contatore vale: {contatore}</h2>
{/if}



<Counter bind:counter={contatore} />




{#if doppio_contatore < 5}
    <h2 class="viola">Il valore del contatore vale: {doppio_contatore}</h2>
{:else}
    <h2 class="arancione">Il valore del contatore vale: {doppio_contatore}</h2>
{/if}
<DoubleCounter bind:counter={doppio_contatore} />




<style>
    .rosso { color: red;}
    .verde { color: green;}
    .viola { color: purple;}
    .arancione { color:darkorange}
</style>


