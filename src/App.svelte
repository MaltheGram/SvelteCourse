<script>
    import AddData from "./components/introduction/AddData.svelte";
    import DynamicAttributes from "./components/introduction/DynamicAttributes.svelte";
    import HTMLTags from "./components/introduction/HTMLTags.svelte";
    import Assignments from "./components/reactivity/Assignments.svelte";
    import Declarations from "./components/reactivity/Declarations.svelte";
    import Statements from "./components/reactivity/Statements.svelte";
    import ArraysAndObjects from "./components/reactivity/ArraysAndObjects.svelte";

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


<style>
    div {
        margin-bottom: 50px;
    }
</style>