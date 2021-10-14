<script lang="ts">
	import { page } from '$app/stores';
</script>

<header>
	<nav>
		<label for="hamburger">&#9776;</label>
		<input type="checkbox" id="hamburger"/>

		<ul id="hamburger-ingredients">
			<li class:active={$page.path === '/design-system'}>
				<a sveltekit:prefetch href="/design-system">Design System</a>
			</li>
			<li class:active={$page.path === '/mythic'}><a sveltekit:prefetch href="/mythic">Mythic</a></li>
			<li class:active={$page.path === '/todos'}><a sveltekit:prefetch href="/todos">Todos</a></li>
			<li class:active={$page.path === '/'}><a sveltekit:prefetch href="/">WX</a></li>
			<li class:active={$page.path === '/about'}><a sveltekit:prefetch href="/about">About</a></li>
		</ul>
	</nav>

	<div class="banner">
		Banner
	</div>
</header>

<style>
	nav label, #hamburger { display: none; }

	nav {
		background-color: var(--color-one);
		display: flex;
		min-height: var(--height-nav);
	}

	nav ul {
		display: flex;
		align-items: center;
	}

	nav ul li {
		list-style: none;
	}

	nav ul li:hover {
		background-color: var(--color-green);
		color: var(--color-black);
	}

	nav ul li.active {
		background-color: var(--color-yellow);
	}

	nav ul li a {
		align-items: center;
		color: var(--color-white);
		display: flex;
		height: var(--height-nav);
		padding-left: 1em;
		padding-right: 1em;
		text-decoration: none;
	}

	nav ul li a:hover {
		color: var(--color-black);
	}

	nav ul li.active a {
		color: var(--color-black);
	}

	@media only screen and (max-width: 425px) {
		nav {
			flex-direction: column;
			height: unset;
		}

		nav label { 
			align-items: center;
			background: var(--color-yellow);
			color: var(--color-black);
			display: flex;
			font-size: 1.5em; 
			height: var(--height-nav);
			justify-content: center;
			padding: 0;
		}

		#hamburger-ingredients { display: none; }
		nav input:checked ~ #hamburger-ingredients { display: block; }

		nav ul {
			display: block;
			flex-direction: column;
			flex-grow: 1;
			
		}

		nav ul li {
			align-items: center;
			display: flex;
			height: var(--height-nav);
			justify-content: center;
			width: 100%;
		}

		nav ul li a {
			align-items: center;
			display: flex;
			flex-grow: 1;
			height: 100%;
			justify-content: center;
		}
	}
</style>