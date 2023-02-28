<script>
    import Add from "../demo/add.svelte";
    import Icon from "./Icon.svelte";
    import Table from "./Table.svelte";
    export let width = '100%';
    export let iconName = 'setting'; 
    export let bodys = [
        {}
    ];
    let selected = 3;
    export let tabs = [
        {
            'index': 0,
            'title':'personnel'
        },
        {
            'index': 1,
            'title':'incident'
        },
        {
            'index': 2,
            'title':'diagno'
        },
        {
            'index': 3,
            'title':'config'
        }
    ]
</script>

<div class="flex border border-gray-300 border-b-0">
    {#each tabs as tab}
        {#if tab.index == selected}    
            <div style:width={width} class="text-white bg-gray-800 flex justify-center px-3 py-5 text-lg active-tab font-semibold">
                <p class="flex items-center"><Icon name={iconName} width={"40px"} /> <span class="px-2">{tab.title}</span></p>
            </div>
        {:else}
            <div style:width={width} class="text-white bg-gray-800 flex justify-center px-3 py-5 text-lg font-semibold">
                <p class="flex items-center"><Icon name={iconName} color='white' width={"40px"} /> <span class="px-2">{tab.title}</span></p>
            </div>
        {/if}      
    {/each}
</div>

<div class="border border-t-0 border-gray-300 p-5 px-5 relative">
    {#each bodys as body, i}
        {#if body.index == selected}
            <Table /> this is {i}
        {/if}
    {/each}

    <!-- <Table /> -->

    <Add />
</div>

<style>
    .active-tab{
        color:#000;
        background-color: rgb(255, 255, 255);
    }
</style>