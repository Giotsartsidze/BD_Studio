<script lang="ts">
    import "../app.css";
	let { children } = $props();
</script>

<svelte:head>
	<link rel="icon" href="/images/logo.svg" />
</svelte:head>

{@render children()}
