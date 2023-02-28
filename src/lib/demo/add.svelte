<script>
    let showBox = false;

    

</script>
{#if showBox}
    <div class="w-[500px] bg-white absolute border border-gray-300 top-10 right-10">
        <div class="flex items-center h-[70px] bg-gray-800 text-white text-2xl px-5">
            <span class="">Add New Element</span>
        </div>
        <div class="flex flex-wrap  h-100 px-[10px] px-[10px]">
        <div class="flex flex-col px-2 py-3">
                <label for="">Title</label>
            <input class="border h-9 w-[220px]" type="text">
        </div>
        <div class="flex flex-col px-2 py-3">
                <label for="">Matriculation</label>
                <input class="border h-9 w-[220px]" type="text">
        </div>
        <div class="w-1/2 flex flex-col mx-2 my-3">
            <label for="">Categorie</label>
                <select class="border h-9 w-[220px]" name="" id="">
                    <option value=""></option>
                    <option value="softwar engeneer">Softwar Engeneer</option>
                    <option value="ui/ux designer">UI/UX Designer</option>
                    <option value="database architect">Database Architect</option>
                </select> 
        </div>
        <div class="w-full px-2 py-3">
                <label for="">Discription</label>
                <textarea class="w-full border" name="" id="" cols="30" rows="8"></textarea>
        </div>
        </div>
        <div class="flex bg-gray-200 flex justify-end">
            <button class="bg-gray-800 text-white px-8 py-3 text-lg">Submite</button>
            <button class="px-8 py-3 bg-gray-300 text-lg">Cancel</button>
        </div>
    </div>
{/if}

<style>

</style>