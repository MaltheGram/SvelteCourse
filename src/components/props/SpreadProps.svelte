<script>
    export let name, version, speed, website

</script>

<!-- In App.svelte we can use the spread operator rather than having to type each of the values -->
<p>
    The <strong>{name}</strong> package is {speed} fast.
    Download version {version} from <a href="https://www.npmjs.com/package/{name}">npm</a>
    and <a href={website}>learn more here</a>
</p>