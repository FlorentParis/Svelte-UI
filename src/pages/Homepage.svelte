<script>
    export let location;
</script>

<div id="page-homepage">
    <section id="hero">
        <h1>Svelte Squirrel: Unlimited Librairy Ressources</h1>
        <img src="./Squirrel.png" alt="Logo svelte-UI" />
    </section>
</div>

<style>
    #page-homepage {
        padding: 0 90px;
    }

    #hero {
        height: calc(100vh - 180px);
        display: flex;
        align-items: center;
        justify-content: space-between;
    }

    #hero > img {
        height: 100%;
    }
</style>