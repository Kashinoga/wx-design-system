<script lang="ts">
	import Header from '$lib/header/header.svelte';
	import '../app.css';
</script>

<Header />

<main>
	<article>
		<slot />
	</article>
</main>

<footer>
	<div class="footer-item">
		<a href="https://kashinoga.com/">Kashinoga</a>
	</div>
</footer>

<style>
	main {
		padding: 1rem;
	}

	footer {
		background-color: var(--color-one);
		display: flex;
		font-size: 0.7em;
		margin-top: auto;
		min-height: var(--height-footer);
	}

	.footer-item {
		margin: auto;
	}

	.footer-item a {
		color: var(--color-white);
	}

	.footer-item a:hover {
		color: var(--color-yellow);
	}
</style>