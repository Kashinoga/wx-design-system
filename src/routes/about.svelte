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
	<h1>WX Design System</h1>

	<h2>Weather Alerts</h2>

	<p>WX is a weather alerts app built on the National Weather Service API and is used here to showcase the WX Design System.</p>

	<h2>Design System</h2>

	<p>WX Design System is currently a hobby project for me to learn web technologies and to build a design language for my other hobby projects.</p>
</div>

<style>
	.content {
		width: 100%;
		max-width: var(--column-width);
		margin: var(--column-margin-top) auto 0 auto;
	}
</style>
