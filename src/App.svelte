<script>
import { Router, Route } from "svelte-routing";
import Navbar from "./components/Navbar.svelte";
import PageDocumentation from "./pages/PageDocumentation/index.svelte";
import PageComponents from "./pages/PageComponents/index.svelte";
import Homepage from "./pages/Homepage.svelte";
import Buttons from "./pages/PageComponents/components/Buttons.svelte";
import Badges from "./pages/PageComponents/components/Badges.svelte";
import Toggle from "./pages/PageComponents/components/Toggle.svelte";
import SelectMenus from "./pages/PageComponents/components/SelectMenus.svelte";
import Headers from "./pages/PageComponents/components/Headers.svelte";
import Sign from "./pages/PageComponents/components/Sign.svelte";
import Tables from "./pages/PageComponents/components/Tables.svelte";
import Notifications from "./pages/PageComponents/components/Notifications.svelte";
import Modals from "./pages/PageComponents/components/Modals.svelte";
import Pagination from "./pages/PageComponents/components/Pagination.svelte";

export let url = "";

</script>

<div id="page-container">
  <Navbar />
  <Router url={url}>
    <Route path="/" component={Homepage} />
    <Route path="documentation" component={PageDocumentation} />
    <Route path="components" component={PageComponents} />

    <Route path="component-buttons" component={Buttons} />
    <Route path="component-badges" component={Badges} />
    <Route path="component-toggle" component={Toggle} />
    <Route path="component-select-menus" component={SelectMenus} />
    <Route path="component-headers" component={Headers} />
    <Route path="component-sign" component={Sign} />
    <Route path="component-tables" component={Tables} />
    <Route path="component-notifications" component={Notifications} />
    <Route path="component-modals" component={Modals} />
    <Route path="component-pagination" component={Pagination} />
  </Router>
</div>

<style>
  :global(body) {
    margin: 0;
    font-family: sans-serif;
  }

  :global(#app) {
    display: flex;
    justify-content: center;
    width: 100%;
  }

  :global(a) {
    text-decoration: none;
    color: #000;
  }

  #page-container {
    max-width: 1920px;
    width: 100%;
    padding: 20px 0 80px 0;
  }
</style>