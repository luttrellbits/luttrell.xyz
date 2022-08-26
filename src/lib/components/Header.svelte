<script>
	import Nav from './Nav.svelte';
</script>

<div id="header">
	<div id="brand">
		<a href="/"> luttrell.xyz </a>
	</div>
	<Nav />
</div>

<style>
	#header {
		display: flex;
		flex-direction: column;
		align-items: center;
		margin: 0 1rem;
	}

	#brand {
		font-size: 1.5rem;
	}

	#brand a {
		color: var(--fg0);
	}

	@media (min-width: 420px) {
		#header {
			flex-direction: row;
			justify-content: space-between;
		}
	}
</style>
