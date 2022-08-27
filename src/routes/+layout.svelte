<script>
	import 'normalize.css';
	import Header from '../lib/components/Header.svelte';
	import Footer from '../lib/components/Footer.svelte';
</script>

<Header />
<main>
	<slot />
</main>
<Footer />

<style global>
	:root {
		--bg0: #2e3440;
		--bg1: #3b4252;
		--bg2: #434c5e;
		--bg3: #4c566a;
		--fg0: #d8dee9;
		--fg1: #e5e9f0;
		--fg2: #eceff4;
		--acc0: #8fbcbb;
		--acc1: #88c0d0;
		--acc3: #81a1c1;
		--blue: #5e81ac;
		--red: #bf616a;
		--orange: #d08770;
		--yellow: #ebcb8b;
		--green: #a3be8c;
		--pink: #b48ead;
		--black: #060606;
	}

	body {
		background-color: var(--bg0);
		color: var(--fg0);
	}
	main {
		margin: 0 2rem;
	}
</style>
