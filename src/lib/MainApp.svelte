<script>
    import { Router, Route } from 'svelte-navigator';
    import Home from './Home.svelte';
</script>

<div class="body">

    <Router basepath={'/'}>
        <Route path="" component={Home} />
    </Router>
    
</div>
