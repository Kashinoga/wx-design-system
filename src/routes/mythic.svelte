<script context="module">
	import { browser, dev } from '$app/env';

	// we don't need any JS on this page, though we'll load
	// it in dev so that we get hot module replacement...
	export const hydrate = dev;

	// ...but if the client-side router is already loaded
	// (i.e. we came here from elsewhere in the app), use it
	export const router = browser;

	// since there's no dynamic data here, we can prerender
	// it so that it gets served as a static asset in prod
	export const prerender = true;
</script>

<svelte:head>
	<title>About | WX Design System</title>
</svelte:head>

<div class="content">
	<h1>Cards</h1>
	<div class="deck">
		<div class="card">
			<div class="card-header">
				<div class="card-header-block-left">
					R
				</div>
				<div class="card-header-text">
					Card
				</div>
			</div>
			<div class="card-content">Content</div>
			<div class="card-footer">
				<div class="card-footer-text">Footer</div>
			</div>
		</div>
	</div>
</div>

<style>
	@media only screen and (max-width: 425px) {
		.deck {
			align-items: center;
			display: flex;
			flex-direction: column;
		}
	}

	.card {
		border: 1px solid black;
		border-radius: 0.3em;
		display: flex;
		flex-direction: column;
		height: 300px;
		width: 200px;
	}

	.card-header {
		border-bottom: 1px dashed black;
		display: flex;
		flex-direction: row;

	}

	.card-header-block-left {
		border-right: 1px dashed black;
		padding: 0.5em;
	}

	.card-header-text {
		padding: 0.5em;
	}

	.card-content {
		padding: 1em;
	}

	.card-footer {
		border-top: 1px dashed black;
		display: flex;
		font-size: 0.8em;
		justify-content: flex-end;
		margin-top: auto;
		padding: 0.2em;
	}
</style>