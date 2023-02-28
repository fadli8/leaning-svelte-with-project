<script>
    import Sidebar from './layouts/sidebar.svelte';
    import Navbar from './layouts/navbar.svelte';
    import Test from './demo/test.svelte';
    import LoginPage from './login/LoginPage.svelte';
    let route = window.location.pathname;
    console.log(route);
</script>

{#if route == '/'}
    <LoginPage />
{:else}
    <Navbar />
    <div class="flex">
        <Sidebar />
        <div class="p-5 w-full">
            
            {#if route == '/home'}
            <Test />
            {/if}
        </div>
    </div>
{/if}