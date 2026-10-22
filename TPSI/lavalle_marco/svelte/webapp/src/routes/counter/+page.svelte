<script>
    import Counter from "../../lib/components/counter.svelte";
    import DoubleCounter from "../../lib/components/DoubleCounter.svelte";
    let contatore = 0;
    let doppio;
    let numeri = [1, 7, 2, 6, 9, 10];
    let sottolineato;

    $:{
        doppio= contatore * 2
        sottolineato = contatore != 7 
    }
</script>


<h2>Pagina Counter</h2>


{#if contatore < 5}
    <h2 class="rosso">Il valore del contatore vale: {contatore}</h2>
{:else}
    <h2 class:sottolineato>Il valore del contatore vale: {contatore}</h2>
{/if}



<Counter bind:counter={contatore} />



{#if doppio < 5}
    <h2 class="viola">Il valore del contatore vale: {doppio}</h2>
{:else}
    <h2 class="arancione">Il valore del contatore vale: {doppio}</h2>
{/if}
<DoubleCounter bind:counter={doppio} />


<ul>
    {#each numeri as numero, indice}
        <li>numeri[{indice}]:{numero}</li>
    {/each}
</ul>


<style>
    .rosso { color: red;}
    .verde { color: green;}
    .viola { color: purple;}
    .arancione { color:darkorange}
    .sottolineato { text-decoration: underline;}
</style>











