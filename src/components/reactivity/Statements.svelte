<script>
    let count = 0

    const handleClick = () => {
        count += 1
    }
    // Statement blocks
    $: {
        console.log("The count is " + count)
        //alert("The count is " + count) This is too annoying for testing
    }

    $: if (count >= 10) {
        alert("Count is really high! Resetting....")
        count = 0
    }
</script>

<button on:click={handleClick}>
    Clicked {count} {count === 1 ? 'time' : 'times'}
</button>
