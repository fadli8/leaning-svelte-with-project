<script>
    import Icon from "../nexus/Icon.svelte";
</script>
<div class="h-full w-1/6 primary-bg-color" style="height:93vh">
    <ul class="pt-7 px-4 pb-2 h-full">
        <p class="mb-10">the first space</p>
        <li class="mx-3 px-1 selected rounded">
            <a class="flex items-center" href="#">
                <Icon name='setting' width="20px" height="20px"/>
                <span class="pl-2">Setting</span>
            </a>
        </li>
        <li class="mx-3 my-3 px-1 py-2 rounded">
            <a class="flex items-center" href="#">
                <Icon name='graph' width="20px" height="20px"/>
                <span class="pl-2">Analytics</span>
            </a>
        </li>
        <li class="mx-3  my-3 px-1 py-2 rounded">
            <a class="flex items-center" href="#">
                <Icon name='setting' width="20px" height="20px"/>
                <span class="pl-2">Setting</span>
            </a>
        </li>
        <li class="mx-3  my-3 px-1 py-2 rounded">
            <a class="flex items-center" href="#">
                <Icon name='setting' width="20px" height="20px"/>
                <span class="pl-2">Setting</span>
            </a>
        </li>
        <li class="mx-3 my-3 px-1 py-2 rounded">
            <a class="flex items-center" href="#">
                <Icon name='setting' width="20px" height="20px"/>
                <span class="pl-2">Setting</span>
            </a>
        </li>
    </ul>
</div>

<style>
    *{
        font-size: 10pt;
    }

    .primary-bg-color{
        background-color: #6366F1;
    }
    .selected{
        padding: 0.3rem 0;
        background-color: #fff;
    }
</style>