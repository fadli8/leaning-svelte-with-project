<script>
    import { onMount } from 'svelte';
    import Icon from './Icon.svelte';

    onMount(  () =>{
        limit();
        // setInterval(()=>{
        //         limit();
        //     }, 3000) 
    })

    export let columns = [
        {
            title: "ID",
            width: "2%",

        },
        {
            title: "Title",
            width: "10%",

        },
        {
            title: "Matriculation",
            width: "10%",

        },
        {
            title: "Discription",
            width: "40%",

        },
        {
            title: "Categorie",
            width: "10%",

        },
        {
            title: "Created at",
            width: "10%",

        },
        {
            title: "Actions",
            width: "10%",

        },
    ];

    let showActions = false;
    $: res = [];

    let data = [
        {
            "ID": 1,
            "Title": "Hello World!",
            "Matriculation": "1548-A-04",
            "Discription": "All about new message in each programming lang",
            "Categorie": "Coding",
            "Created_at" : "06-02-2023 15:47",
        },
        {
            "ID": 2,
            "Title": "Hello World!",
            "Matriculation": "1548-A-04",
            "Discription": "All about new message in each programming lang",
            "Categorie": "Coding",
            "Created_at" : "06-02-2023 15:47",
        },
        {
            "ID": 3,
            "Title": "Hello World!",
            "Matriculation": "1548-A-04",
            "Discription": "All about new message in each programming lang",
            "Categorie": "Coding",
            "Created_at" : "06-02-2023 15:47",
        },
        {
            "ID": 4,
            "Title": "Hello World!",
            "Matriculation": "1548-A-04",
            "Discription": "All about new message in each programming lang",
            "Categorie": "Coding",
            "Created_at" : "06-02-2023 15:47",
        }
    ];

    function limit(){
        res = data.map(el => el)
    }
</script>
<div class="flex justify-between border border-gray-300 border-b-0 px-2 py-3 bg-gray-200 w-full">
    <div class="flex items-center">
        <Icon name="filter" width={"40px"} /> <span class="text-lg px-2">Filter</span> <Icon name="add" />
    </div>
    <div class="others">
        this is the others
    </div>
</div>
<div class="w-full">
    <table class="table-border w-full">
        <thead>
            <tr>
                {#each columns as c}
                    <th width={c.width} class='py-1 text-sm h-10 bg-gray-200'>{c.title}</th>    
                {/each}
            </tr>
        </thead>
        <tbody>
            {#if res.length != 0}
                {#each res as row}        
                    <tr class="text-md px-2">
                        <td class="h-10 px-2">{row.ID}</td>
                        <td class="h-10 px-2">{row.Title}</td>
                        <td class="h-10 px-2">{row.Matriculation}</td>
                        <td class="h-10 px-2">{row.Discription}</td>
                        <td class="h-10 px-2">{row.Categorie}</td>
                        <td class="h-10 px-2">{row.Created_at}</td>
                        <td>
                            <div class="flex justify-center">
                                <Icon name="more" />
                            </div>
                        </td>
                    </tr>

                    {#if showActions}
                        <span class="w-[150px] absolute flex flex-col bg-white pt-2 ty-3 right-0 m-0">
                            <ul>
                                <li>Add</li>
                                <li>Update</li>
                                <li>Delete</li>
                            </ul>
                        </span>
                    {/if}
                {/each}
            {:else}
            <tr class="text-md px-2">
               
                <td colspan={7}>
                    <div class="flex justify-center p-5 ">
                       There are not data to show!
                    </div>
                </td>
            </tr>
            {/if}
        </tbody>
        
    </table>
    <div class="flex justify-between px-3 py-1 border border-t-0 border-gray-300 bg-gray-50">
        <div class="flex">
            <select class="border rounded-md px-1" name="" id="">
                <option value="10">10</option>
                <option value="25">25</option>
                <option value="50">50</option>
                <option value="100">100</option>
            </select>
            <span class="px-3">Total Row : {data.length}</span>
        </div>
        <div class="flex">
            <label class="px-1" for="">Pages :</label><input class="border rounded-md px-1 w-10 text-center" type="number" name="" id=""><span class="px-1">of {Math.round(data.length/5)}</span>
            <button>Previus</button>
            <button>Next</button>
        </div>
    </div>
</div>

<style>

    .table-border th,.table-border td{
        border:1px solid #d1d1d1;
    }
        
</style>