<script>
	import '$lib/styles/app.css';
	import Sidebar from '$lib/components/Sidebar.svelte';
</script>

<svelte:head>
	<title>PERFORMER AI</title>
</svelte:head>

<div class="flex">
	<Sidebar />
	<span><slot /></span>
</div>
