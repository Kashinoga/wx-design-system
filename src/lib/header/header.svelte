<script lang="ts">
	import { page } from '$app/stores';
</script>

<header>
	<nav>
		<ul class="mobile-nav">
			<li class="badge" class:active={$page.path === '/'}><a sveltekit:prefetch href="/">WX</a></li>
			<li class:active={$page.path === '/welcome'}>
				<a sveltekit:prefetch href="/welcome">Welcome</a>
			</li>
			<li class:active={$page.path === '/about'}><a sveltekit:prefetch href="/about">About</a></li>
			<li class:active={$page.path === '/todos'}><a sveltekit:prefetch href="/todos">Todos</a></li>
		</ul>

		<ul class="nav">
			<li class="badge" class:active={$page.path === '/'}><a sveltekit:prefetch href="/">WX</a></li>
			<li class:active={$page.path === '/welcome'}>
				<a sveltekit:prefetch href="/welcome">Welcome</a>
			</li>
			<li class:active={$page.path === '/about'}><a sveltekit:prefetch href="/about">About</a></li>
			<li class:active={$page.path === '/todos'}><a sveltekit:prefetch href="/todos">Todos</a></li>
		</ul>
	</nav>
</header>

<style>
	nav {
		background-color: var(--color-one);
		display: flex;
	}

	.badge {
		background-color: var(--color-yellow);
	}

	.badge a {
		color: var(--color-black);
	}

	.mobile-nav {
		display: none;
	}

	@media only screen and (max-width: 425px) {
		.mobile-nav {
			display: block;
			flex-direction: column;
			flex-grow: 1;
		}

		.nav {
			display: none;
		}
	}

	nav ul {
		display: flex;
	}

	nav ul li {
		list-style: none;
	}

	nav ul li:hover {
		background-color: var(--color-green);
		color: var(--color-black);
	}

	nav ul li a {
		color: var(--color-white);
		display: block;
		padding: 1em;
		text-decoration: none;
	}

	nav ul li a:hover {
		color: var(--color-black);
	}
</style>