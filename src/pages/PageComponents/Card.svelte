<script>
    import { navigate } from "svelte-routing";

    export let title;
    export let img;
    export let url;

</script>

<div id="card" on:click={() => navigate(url, { replace: false })}>
    <img src={img} alt="" />
    <span>{title}</span>
</div>

<style>
    #card {
        padding: 10px;
        border-radius: 5px;
        box-shadow: rgba(149, 157, 165, 0.2) 0px 8px 24px;
        cursor: pointer;
    }

    img {
        width: 100%;
    }
</style>