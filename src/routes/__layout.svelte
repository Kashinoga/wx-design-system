<script lang="ts">
	import Header from '$lib/header/header.svelte';
	import '../app.css';
</script>

<Header />

<div class="content">
	<slot />
</div>

<footer>
	<div class="footer-item">
		<p>
			<a href="https://kashinoga.com/">Kashinoga</a>
		</p>
	</div>
</footer>

<style>
	.content {
		/* height: calc(100% - ) */
		padding: 1rem;
	}

	footer {
		background-color: var(--color-one);
		display: flex;
	}

	.footer-item {
		margin: auto;
	}

	.footer-item p a {
		color: var(--color-white);
	}

	.footer-item p a:hover {
		color: var(--color-yellow);
	}
</style>