<script lang="ts">
	import { page } from '$app/stores';
	import logo from '/static/icons8-wind-16.png';
</script>

<header>
	<div class="corner">
		<a href="/">
			<img src={logo} alt="WX" />
		</a>
	</div>

	<nav>
		<!-- <svg viewBox="0 0 2 3" aria-hidden="true">
			<path d="M0,0 L1,2 C1.5,3 1.5,3 2,3 L2,0 Z" />
		</svg> -->
		<ul>
			<li class:active={$page.path === '/'}><a sveltekit:prefetch href="/">WX</a></li>
			<li class:active={$page.path === '/welcome'}>
				<a sveltekit:prefetch href="/welcome">Welcome</a>
			</li>
			<li class:active={$page.path === '/about'}><a sveltekit:prefetch href="/about">About</a></li>
			<li class:active={$page.path === '/todos'}><a sveltekit:prefetch href="/todos">Todos</a></li>
		</ul>
		<!-- <svg viewBox="0 0 2 3" aria-hidden="true">
			<path d="M0,0 L0,3 C0.5,3 0.5,3 1,2 L2,0 Z" />
		</svg> -->
	</nav>

	<!-- <div class="corner">
		
	</div> -->
</header>

<style>
	header {
		display: flex;
		flex-direction: row;
		/* justify-content: space-between; */
	}

	.corner {
		background: var(--color-yellow);
		flex: none;
		width: 3em;
		height: 3em;
	}

	.corner a {
		display: flex;
		align-items: center;
		justify-content: center;
		width: 100%;
		height: 100%;
	}

	.corner img {
		height: auto;
		object-fit: fit;
		width: auto;
	}

	nav {
		display: flex;
		flex: auto;
		/* justify-content: center; */
		background: var(--color-bg);
	}

	svg {
		width: 2em;
		height: 3em;
		display: block;
	}

	path {
		fill: var(--background);
	}

	ul {
		position: relative;
		padding: 0;
		margin: 0;
		height: 3em;
		display: flex;
		justify-content: center;
		align-items: center;
		list-style: none;
		background: var(--background);
		background-size: contain;
	}

	li {
		flex: auto;
		position: relative;
		height: 100%;
	}

	li.active::before {
		--size: 8px;
		content: '';
		width: 0;
		height: 0;
		position: absolute;
		bottom: 0;
		left: calc(50% - var(--size));
		border: var(--size) solid transparent;
		border-bottom: var(--size) solid var(--color-yellow);
	}

	nav a {
		display: flex;
		height: 100%;
		align-items: center;
		padding: 0 1em;
		color: var(--color-white);
		/* font-weight: 600; */
		/* font-size: 0.8rem; */
		/* text-transform: uppercase; */
		/* letter-spacing: 0.01em; */
		text-decoration: none;
		/* transition: color 0.2s linear; */
	}

	a:hover {
		color: var(--color-yellow);
	}

	li a:active:hover {
		color: var(--color-white);
	}
</style>
