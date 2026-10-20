<script>
    import Counter from "../../lib/components/counter.svelte";
    import DoubleCounter from "../../lib/components/DoubleCounter.svelte";
    let contatore = 0;
    let doppio_contatore = 0;
</script>


<h2>Pagina Counter</h2>
<h3>il valore del contatore vale: {contatore}</h3>
<Counter bind:counter={contatore} />

<h3>il valore del contatore vale: {doppio_contatore}</h3>
<DoubleCounter bind:counter={doppio_contatore} />