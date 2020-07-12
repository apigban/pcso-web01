<script>
  import Select from "svelte-select";
  import Games from "./GamesList.json";
  // import Content from './Content.svelte';
  // import Sidebar from './Sidebar.svelte';
  import Combine from "./Combine.svelte";

  let open = false;
  const items = Games.gamename;
</script>

<Combine />
<!-- <Sidebar />
<Content /> -->
<!-- 
<Sidebar bind:open/>
<NavBar bind:sidebar={open}/> -->

<!-- <h2>Default</h2>
<Select {items}></Select> -->
