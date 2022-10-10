<script>
    let numbers = [0, 1, 2, 4]

    /*
     clicking the "Add a number" button calls the addNumber
     function, which appends a number to the array but doesn't trigger the recalculation of sum.
     One way to fix that is to assign numbers to itself to tell the compiler it has changed
     */

    const addNumber = () => {
        numbers = [...numbers, numbers.length + 1]
    }
    $: sum = numbers.reduce((t, n) => t + n, 0);

</script>

<p>{numbers.join(' + ')} = {sum}</p>
<button on:click={addNumber}>
    Add a number
</button>