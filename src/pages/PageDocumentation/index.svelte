<script>
    import NavAside from "./NavAside.svelte";
    
    let docChoice;

    export let location;
</script>

<div id="page-documentation">
    <NavAside />
    <div>
        <h1>Set-up</h1>
        <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit. Sequi ullam tenetur iste ad! Ducimus odio error laboriosam. Modi quae necessitatibus praesentium, nulla obcaecati magni, eos iure et harum minima unde?</p>
        <h1>Nanana</h1>
        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Perspiciatis dignissimos pariatur autem? Dolorum expedita exercitationem, non odio rerum, placeat voluptas, deserunt accusamus excepturi veniam aperiam hic laborum velit est incidunt?
        Modi nulla ea minus nesciunt voluptas, velit dolor soluta, non maiores quia porro? Veritatis nemo delectus aliquam explicabo harum nesciunt molestiae, repellendus alias nisi hic incidunt. Aliquam corporis impedit id!
        Ducimus alias fugit fuga doloribus incidunt mollitia dolor blanditiis consequatur. Praesentium excepturi ab pariatur modi impedit tempore ex maiores, numquam laborum! Quae, veritatis id vel recusandae sunt sequi beatae fugit.
        Dolorum molestiae aliquid non illum corrupti deserunt impedit ipsam quo quos reprehenderit tempore neque exercitationem hic dicta, corporis, culpa sapiente perferendis repudiandae iusto? Perferendis, nostrum voluptates adipisci reiciendis atque aperiam!
        </p>
        <h1>Blabla</h1>
        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. At id officia cumque, dolorum minima perspiciatis explicabo quas. Animi, modi dolorem. Quisquam odit eligendi repellat quam voluptatum possimus perferendis maiores minus?
        Excepturi nobis et fugit! Itaque maiores ab sequi assumenda perspiciatis deserunt eaque inventore quo reprehenderit! Laborum dolores corrupti cum accusamus tempora ratione assumenda labore ipsa incidunt aspernatur, quidem saepe fugit!</p>
    </div>
</div>

<style>
    #page-documentation {
        display: grid;
        grid-template-columns: 1fr 3fr;
        padding: 20px 90px 0 0;
    }
</style>