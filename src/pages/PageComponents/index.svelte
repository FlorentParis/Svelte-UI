<script>
import Card from "./Card.svelte";

</script>

<div id="page-container">
    <Card title="Buttons" url="component-buttons" img="https://tailwindui.com/img/category-thumbnails/application-ui/buttons.png" />
    <Card title="Badges" url="component-badges" img="https://tailwindui.com/img/category-thumbnails/application-ui/badges.png" />
    <Card title="Toggle" url="component-toggle" img="https://tailwindui.com/img/category-thumbnails/application-ui/toggles.png" />
    <Card title="Select Menus" url="component-select-menus" img="https://tailwindui.com/img/category-thumbnails/application-ui/select-menus.png" />
    <Card title="Headers" url="component-headers" img="https://tailwindui.com/img/category-thumbnails/marketing/headers.png" />
    <Card title="Sign-in & Registration" url="component-sign" img="https://tailwindui.com/img/category-thumbnails/application-ui/sign-in-forms.png" />
    <Card title="Tables" url="component-tables" img="https://tailwindui.com/img/category-thumbnails/application-ui/tables.png" />
    <Card title="Notifications" url="component-notifications" img="https://tailwindui.com/img/category-thumbnails/application-ui/notifications.png" />
    <Card title="Modals" url="component-modals" img="https://tailwindui.com/img/category-thumbnails/application-ui/modals.png" />
    <Card title="Pagination" url="component-pagination" img="https://tailwindui.com/img/category-thumbnails/application-ui/pagination.png" />
</div>

<style>
    #page-container {
        padding: 0 90px;
        display: grid;
        grid-template-columns: repeat(4, 1fr);
        gap: 20px;
    }
</style>