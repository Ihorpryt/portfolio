<script>
	import { page } from '$app/stores';
	import logo from '$lib/images/svelte-logo.svg';
	import github from '$lib/images/github.svg';
</script>

<header>
	<!-- <div class="corner">
		<a href="https://kit.svelte.dev">
			<img src={logo} alt="SvelteKit" />
		</a>
	</div> -->

	<nav>
		<ul>
			<li aria-current={$page.url.pathname === '/' ? 'page' : undefined}>
				<a href="/">Portfolio</a>
			</li>
			<li aria-current={$page.url.pathname === '/about' ? 'page' : undefined}>
				<a href="/about">About</a>
			</li>
			<li aria-current={$page.url.pathname.startsWith('/resources') ? 'page' : undefined}>
				<a href="/resources">Resources</a>
			</li>
			<li aria-current={$page.url.pathname.startsWith('/contact') ? 'page' : undefined}>
				<a href="/contact">Contact</a>
			</li>
		</ul>
	</nav>

	<!-- <div class="corner">
		<a href="https://github.com/sveltejs/kit">
			<img src={github} alt="GitHub" />
		</a>
	</div> -->
</header>

<style>
	header {
		display: flex;
		justify-content: space-between;
	}

	nav {
		display: flex;
		justify-content: center;
		position: fixed;
    	bottom: 16px;
		width: 100%;
		height: 60px;
 		max-width: 500px;
		left: 50%;
		-webkit-transform: translate(-50%, -24px);
		transition: transform .4s cubic-bezier(.165,.84,.44,1);
		transform: translate(-50%);

		-webkit-backdrop-filter: blur(16px);
		backdrop-filter: blur(16px);
		background-color: rgba(246,246,246,.5);
		border-radius: 60px;
	}



	ul {
		position: relative;
		padding: 0px 48px;
		margin: 0;
		width: 100%;
		display: flex;
		justify-content: space-between;
		align-items: center;
		list-style: none;
		background: var(--background);
		background-size: contain;
	}

	li {
		/* position: relative;
		height: 100%; */
		padding: 12px 24px;
	}

	/* li[aria-current='page']::before {
		--size: 6px;
		content: '';
		width: 0;
		height: 0;
		position: absolute;
		top: 0;
		left: calc(50% - var(--size));
		border: var(--size) solid transparent;
		border-top: var(--size) solid var(--color-theme-1);
	} */
	li[aria-current='page'] {
		background-color: white;
		border-radius: 200px;
	}

	nav a {
		font-family: MontrealBook;
		display: flex;
		align-items: center;
		padding: 0 0.5rem;
		color: var(--color-text);
		font-weight: 700;
		font-size: 16px;
		text-decoration: none;
		transition: color 0.2s linear;
	}

	a:hover {
		color: var(--color-theme-1);
	}
</style>
