<script>
	import Select from 'svelte-select';
	import Games from "./GamesList.json";

	const items = Games.gamename;
</script>

<h2>Default</h2>
<Select {items}></Select>
