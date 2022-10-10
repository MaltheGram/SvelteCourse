<script>
    import AddData from "./components/introduction/AddData.svelte";
    import DynamicAttributes from "./components/introduction/DynamicAttributes.svelte";
    import HTMLTags from "./components/introduction/HTMLTags.svelte";
    import Assignments from "./components/reactivity/Assignments.svelte";
    import Declarations from "./components/reactivity/Declarations.svelte";
    import Statements from "./components/reactivity/Statements.svelte";
    import ArraysAndObjects from "./components/reactivity/ArraysAndObjects.svelte";
    import Props from "./components/props/Props.svelte";
    import SpreadProps from "./components/props/SpreadProps.svelte";
    import IfBlocks from "./components/Logic/IfBlocks.svelte";
    import ElseBlocks from "./components/Logic/ElseBlocks.svelte";
    import ElseIfBlocks from "./components/Logic/ElseIfBlocks.svelte";
    import EachBlocks from "./components/Logic/EachBlocks.svelte";
    import KeyedEachBlocks from "./components/Logic/KeyedEachBlocks.svelte";
    import AwaitBlocks from "./components/Logic/AwaitBlocks.svelte";

    const pkg = {
        name: "Svelte",
        version: 3,
        speed: "blazing",
        website: "https://svelte.dev"
    }

    let things = [
        { id: 1, name: 'apple' },
        { id: 2, name: 'banana' },
        { id: 3, name: 'carrot' },
        { id: 4, name: 'doughnut' },
        { id: 5, name: 'egg' },
    ]

    const handleClick = () => {
        things = things.slice(1)
    }

</script>

<div>
    <h1>Introduction</h1>
    <AddData/>
    <DynamicAttributes/>
    <HTMLTags/>
</div>

<div>
    <h1>Reactivity</h1>
    <Assignments/>
    <Declarations/>
    <Statements/>
    <ArraysAndObjects/>

</div>

<div>
    <h1>Props</h1>
    <Props/>
    <Props answer="{35}"/>
    <!--We could also do pkg.name, pkg.version etc, but spread operator is better for Svelte-->
    <SpreadProps {...pkg}/>
</div>

<div>
    <h1>Logic</h1>
    <!-- <IfBlocks/> -->
    <ElseBlocks/>
    <ElseIfBlocks/>
    <EachBlocks/>

    <button on:click={handleClick}>Remove thing</button>
    {#each things as thing (thing.id)}
        <KeyedEachBlocks name="{thing.name}"/>
    {/each}
    <AwaitBlocks/>


</div>


<style>
    div {
        margin-bottom: 50px;
    }
</style>