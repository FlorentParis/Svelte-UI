<script>
    import { Router, Link} from "svelte-routing";
    export let url = "";

    const textDecoration = {
        textDecoration: 'none'
    }
</script>

<nav>
    <Router url={url}>
        <Link to="">Svelte Squirrel</Link>
    
        <div id="nav-links">
            <Link to="/components">Components</Link>
            <Link to="/documentation">Documentation</Link>
            <input type="text" placeholder="Find anything...">
        </div>
    </Router>
</nav>

<style>
    nav {
        display: flex;
        justify-content: space-between;
        align-items: center;
        padding: 0 90px;
        height: 80px;
    }

    #nav-links {
        display: flex;
        gap: 20px;
        list-style: none;
    }
</style>