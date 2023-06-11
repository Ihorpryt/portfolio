<script>
	import { page } from '$app/stores';

	let scrollPosition = 0;

</script>

<svelte:window bind:scrollY={scrollPosition}/>


	<header>
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

		{#if scrollPosition > 700}
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
		   	<a href="#">
		   		<div class="btn">Contact (email) ►</div>
			</a>
		</div>
	   {/if}
	</header>
	


<style>

	.sticky {
		padding:0 48px;
		display: flex;
		justify-content: space-between;
		align-items: center;
		background: rgba(255, 255, 255, 0.01);
		-webkit-backdrop-filter: saturate(180%) blur(20px);
		backdrop-filter: saturate(180%) blur(8px);
		position: fixed;
		height: 40px;
		top: 0;
		left:0;
		right: 0;
		animation-duration: 0.3s;
  		animation-name: slidein;
	}
	.sticky a {
		font-size: 14px;
	}

	.sticky li {
		margin-right: 24px;
	}

	.sticky:after {
		content: "";
		display: block;
		position: absolute;
		top: 100%;
		left: 0;
		width: 100%;
		height: 1px;
		z-index: 1;
		background: rgba(0,0,0,1);
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
			
		}

		to {
			opacity: 1;
			
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
	.btn {
		background-color: #1d1d1f;
		border-radius: 20px;
		color: white;
		border: none;
		font-family: 'MontrealMedium';
		font-size: 12px;
		padding: 6px 12px;
		z-index: 5;
		text-decoration: none;
		text-transform: uppercase;
	}
	.btn:hover {
		background-color: #272729;
	}
	a {
		text-decoration: none;
	}
</style>
