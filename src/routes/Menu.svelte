
<script>
	import { page } from '$app/stores';
	let y;
	
</script>

	<svelte:window bind:scrollY={y} />

	<header class:bottom={y != 0}>
		<nav>
			<ul>
				<div class="shine"></div>
				<li aria-current={$page.url.pathname === '/' ? 'page' : undefined}>
					<a href="{$page.url.pathname === '/' ? '#portfolio' : '/#portfolio'}">Work</a>
				</li>
				<li aria-current={$page.url.pathname === '/about' ? 'page' : undefined}>
					<a href="/about">Info</a>
				</li>
				<li aria-current={$page.url.pathname.startsWith('#') ? 'page' : undefined}>
					<a href="#">Email</a>
				</li>
				<li aria-current={$page.url.pathname.startsWith('#') ? 'page' : undefined}>
					<a href="#">CV</a>
				</li>
			</ul>
		</nav>
	</header>
	


<style>
	header {
		position:fixed;
		left: 50%;
		right: 50%;
		bottom: 96px;
		justify-content:center;
		/* opacity: 0;
		animation: fade 1s forwards;  */
		animation-delay: 3s;
		transition: bottom 0.3s;

		z-index: 50;
	}
	@keyframes fade {
		0% {
			opacity: 0;
		}
		100% {
			opacity: 1;
		}
	}

	nav {
		display: flex;
		justify-content: center;
		height: 64px;
	}

	.bottom {
		bottom: 24px;
	}
	.bottom nav {
		height: 48px;
	}

	.bottom nav a {
		animation: shrink 0.3s forwards;
		animation-delay: 0.3s;
	}

	
	ul {
		margin: 0;
		padding: 12px;
		display: flex;
		justify-content: center;
		align-items: center;
		list-style: none;
		/* background-color: #333; */
		background-color: rgba(22, 22, 23, .5);
		backdrop-filter: saturate(300%) blur(20px) invert(70%) brightness(160%);
		border-radius: 100px;
		gap: 8px;
		filter: drop-shadow(0px 10px 12px rgba(0, 0, 0, 0.5));
		
		/* box-shadow: inset -10px 4px 15px rgba(255, 255, 255, 0.5); */
		/* border: 1px solid rgb(255 255 255 / 8%); */
	}
	.shine {
		height: 1px;
		width: 400px;
		background: linear-gradient(90deg, rgba(172, 171, 171, 0), #ffffff 20%, #ffffff 67.19%, rgba(0, 0, 0, 0));
		z-index: 99;
		top: -1px;
		opacity: 0.6;
		position: absolute;
	}
	li {
		height: 100%;
		display: flex;
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
	}

	nav a {
		font-family: 'MontrealMedium';
		display: flex;
		align-items: center;
		padding: 0 0.5rem;
		color: white;
		font-size:14px;
		text-decoration: none;
		-webkit-font-smoothing: antialiased;
/* 
		background-color: rgba(255, 255, 255, 0.151);
		box-shadow: inset 0.5px 0.5px 0px rgba(255, 255, 255, 0.35), inset 0px 0px 0.5px 1px rgba(255, 255, 255, 0.05); */
		/* text-transform: uppercase; */

		display: flex;
		justify-content: center;
		width: 150px;
		border-radius: 200px;
		transition: 0.3s;
		/* border: 1px solid rgba(255, 255, 255, 0.151); */

		animation: shrink-back 0.3s forwards;

	}

	a:hover {
		background-color: rgba(255, 255, 255, 0.15);

		/* background-color: rgba(255, 255, 255, 0.151); */
		box-shadow: inset 0.5px 0.5px 0px rgba(255, 255, 255, 0.35), inset 0px 0px 12px 1px rgba(255, 255, 255, 0.15);
	}
	
	/* Animations */

	/* - Menu */
	@keyframes shrink {
		from {width: 150px;}
		to {width: 80px;}
	}
	@keyframes shrink-back {
		from {width:80px;}
		to {width: 150px;}
	}
	/* - Menu */

	/* Animations */
</style>
