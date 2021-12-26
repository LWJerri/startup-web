<script lang="ts">
  import { Route, Router } from "svelte-navigator";
  import Main from "./pages/Main.svelte";
  import Example from "./pages/Example.svelte";
</script>

<Router>
  <main>
    <Route path="example/:id" component={Example} />
    <Route component={Main} />
  </main>
</Router>
