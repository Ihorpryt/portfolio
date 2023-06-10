<script>
	import { page } from '$app/stores';

	let scrollPosition = 0;

</script>

<svelte:window bind:scrollY={scrollPosition}/>


	<header>
		{#if scrollPosition < 580}
		<nav>
			<ul>
				<li aria-current={$page.url.pathname === '/' ? 'page' : undefined}>
					<a href="{$page.url.pathname === '/' ? '#main' : '/'}">Start <span class="ua-description">&nbsp &nbsp⁄ старт</span></a>
				</li>
				<li aria-current={$page.url.pathname === '/' ? 'page' : undefined}>
					<a href="{$page.url.pathname === '/' ? '#portfolio' : '/#portfolio'}">Portfolio <span class="ua-description">&nbsp &nbsp⁄ портфоліо</span></a>
				</li>
				<li aria-current={$page.url.pathname === '/about' ? 'page' : undefined}>
					<a href="/about">About <span class="ua-description">&nbsp &nbsp⁄ про мене</span></a>
				</li>
				<li aria-current={$page.url.pathname.startsWith('/resources') ? 'page' : undefined}>
					<a href="/resources">Resources <span class="ua-description">&nbsp &nbsp⁄ ресурси</span></a>
				</li>
			</ul>
		</nav>
		{/if}
		{#if scrollPosition > 580}
		<div class="sticky">
		   <nav>
			   <ul>
				   <li aria-current={$page.url.pathname === '/' ? 'page' : undefined}>
					   <a href="{$page.url.pathname === '/' ? '#main' : '/'}">Start <span class="ua-description">&nbsp &nbsp⁄ старт</span></a>
				   </li>
				   <li aria-current={$page.url.pathname === '/' ? 'page' : undefined}>
					   <a href="{$page.url.pathname === '/' ? '#portfolio' : '/#portfolio'}">Portfolio <span class="ua-description">&nbsp &nbsp⁄ портфоліо</span></a>
				   </li>
				   <li aria-current={$page.url.pathname === '/about' ? 'page' : undefined}>
					   <a href="/about">About <span class="ua-description">&nbsp &nbsp⁄ про мене</span></a>
				   </li>
				   <li aria-current={$page.url.pathname.startsWith('/resources') ? 'page' : undefined}>
					   <a href="/resources">Resources <span class="ua-description">&nbsp &nbsp⁄ ресурси</span></a>
				   </li>
			   </ul>
		   </nav>
		</div>
	   {/if}
	</header>
	


<style>

	.sticky {
		background: red;
		position: fixed;
		width: 100%;
		height: 48px;
		top: 0;
		left:0px;
		animation-duration: 0.3s;
  		animation-name: slidein;
	}

	header {
		display: flex;
		justify-content: space-between;
		transition: 0.3s;
		opacity: 1;
	}

	nav {
		display: flex;
		justify-content: center;
    	bottom: 74px;
		transition: transform .4s cubic-bezier(.165,.84,.44,1);

		animation-duration: 0.3s;
  		animation-name: slidein;
	}

	@keyframes slidein {
		from {
			opacity: 0;
			margin-top: -48px;
		}

		to {
			opacity: 1;
			margin-top: 0;
		}
	}


	ul {
		position: relative;
		padding: 0;
		margin: 0;
		width: 100%;
		display: flex;
		justify-content: space-between;
		align-items: flex-end;
		list-style: none;
		background: var(--background);
		background-size: contain;
	}

	li {
		/* position: relative;
		height: 100%; */
		/* padding: 12px 24px; */
		margin-right: 54px;
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
		color: brown;
		border-radius: 200px;
	}

	nav a {
		font-family: 'MontrealMedium';
		display: flex;
		align-items: center;
		padding: 0 0.5rem;
		color: var(--color-text);
		font-size: 16px;
		text-decoration: none;
		transition: color 0.2s linear;
		-webkit-font-smoothing: antialiased;
	}

	a:hover {
		color: var(--color-theme-1);
	}
	.ua-description {
		opacity: 0.5;
		font-family: 'MontrealBook';
	}
</style>
