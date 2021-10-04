<script lang="ts">
	import { page } from '$app/stores';
</script>

<header>
	<nav>
		<label for="hamburger">&#9776;</label>
		<input type="checkbox" id="hamburger"/>

		<ul id="hamburger-ingredients">
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
	nav label, #hamburger { display: none; }

	nav {
		background-color: var(--color-one);
		display: flex;
		min-height: 70px;
	}

	.badge {
		background-color: var(--color-yellow);
	}

	.badge a {
		color: var(--color-black);
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

	nav ul li a {
		align-items: center;
		color: var(--color-white);
		display: flex;
		height: 70px;
		padding-left: 1em;
		padding-right: 1em;
		text-decoration: none;
	}

	nav ul li a:hover {
		color: var(--color-black);
	}

	@media only screen and (max-width: 425px) {
		nav {
			flex-direction: column;
			height: unset;
		}

		nav label { 
			align-items: center;
			display: flex; 
			color: var(--color-black);
			background: var(--color-yellow);
			height: 70px;
			justify-content: center;
			padding: 0;
		}

		#hamburger-ingredients { display: none; }
		nav input:checked ~ #hamburger-ingredients { display: block; }

		.badge {
			background: var(--color-green);
		}

		nav ul {
			display: block;
			flex-direction: column;
			flex-grow: 1;
			
		}

		nav ul li {
			align-items: center;
			display: flex;
			height: 70px;
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