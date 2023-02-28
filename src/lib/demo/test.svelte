<script>
    import Tabs from "../nexus/Tabs.svelte";
    let bodys = [
        {
            'index': 0,
        },
        {
            'index': 1,
        },
        {
            'index': 2,
        },
        {
            'index': 3,
        }
    ]

</script>
<h1>Title of the page</h1>

<!-- <Table /> -->
<Tabs {bodys} />