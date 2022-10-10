<script>
    const getRandomNumber = async () => {
        const res = await fetch("https://www.randomnumberapi.com/api/v1.0/randomnumber")
        const text = await res.text()

        if (res.ok) {
            return text
        } else {
            throw new Error(text)
        }
    }
    let promise = getRandomNumber();

    const handleClick = () => {
        promise = getRandomNumber()
    }
</script>

<button on:click={handleClick}>
    generate random number
</button>


{#await promise}
    <p>Waiting</p>
{:then number}
    <p>The random number is {number}</p>
{/await}