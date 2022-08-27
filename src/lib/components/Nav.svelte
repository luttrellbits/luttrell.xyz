<nav>
	<input type="checkbox" id="check-btn" />
	<label for="check-btn">
		<div />
		<div />
		<div />
	</label>

	<ul>
		<li><a href="/">Home</a></li>
		<li><a href="/about">About</a></li>
	</ul>
</nav>

<style>
	nav {
		/* items is the number of nav items*/
		--items: 2;
		--height: calc(var(--items) * 1.8rem);
		display: flex;
		flex-direction: column-reverse;
	}
	ul {
		list-style: none;
		display: flex;
		flex-direction: column;
		gap: 1rem;
		padding: 0;
		max-height: 0;
		transition: max-height 0.3s;
		overflow: hidden;
	}
	a {
		color: var(--fg0);
		text-decoration: none;
	}
	a:hover {
		text-decoration: underline;
	}
	input {
		display: none;
	}

	input:checked ~ ul {
		max-height: var(--height);
	}
	input:checked ~ label div:first-child {
		transform: translateY(11px) rotate(45deg);
	}
	input:checked ~ label div:last-child {
		transform: translateY(-11px) rotate(-45deg);
	}
	input:checked ~ label div:nth-child(2) {
		opacity: 0;
	}

	label {
		background-color: var(--bg3);
		border-radius: 3px;
		display: flex;
		flex-direction: column;
		align-items: center;
		justify-content: center;
		width: 50px;
		height: 50px;
	}

	label div {
		background-color: var(--fg0);
		width: 75%;
		height: 3px;
		margin: 4px;
		border-radius: 5px;
		transition: transform 0.3s, opacity 0.3s;
	}

	@media screen and (min-width: 360px) {
		ul {
			flex-direction: row;
			max-height: 1.8rem;
		}
		label {
			display: none;
		}
	}
</style>
