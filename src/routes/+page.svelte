<script>
	import welcome from '$lib/images/svelte-welcome.webp';
	import welcome_fallback from '$lib/images/svelte-welcome.png';

	import { animate } from "motion";
	import { onMount } from 'svelte';
	

	onMount(() => {
		animate(
			".blink",
			{ opacity: [1,0,1] },
  			{ duration: 3, repeat: Infinity },
			);

		animate(
			".bg-cover",
			{ x: '-100vw' },
  			{ duration: 0.5, delay: 1, allowWebkitAcceleration: true },
			);	
	});
	



</script>

<svelte:head>
	<title>Home</title>
	<meta name="description" content="Svelte demo app" />
</svelte:head>




<div class="bg-cover">Hello, I'm Ihor</div>

<section>
	<p class="logo-name smooth" style="text-transform: uppercase;"><span class="blink" style="color:#34c759;">●</span> Ihor</p>
	<div class="avatar"></div>
	<h1>Senior UX/UI Designer,<br />Product Designer</h1>


	<div class="hero-image"></div>

	<div class="work-row">
		<div class="work-element work1">ExpensePulse™ (Portside)</div>
		<div class="work-element work2">PAX App (Airshare/Portside)</div>
	</div>
	<div class="work-row">
		<div class="work-element work3">Staffing Marketplace (JetAviation/Portside)</div>
		<div class="work-element work4">Dynamo Kyiv (Linecore)</div>
	</div>
	<div class="work-row">
		<div class="work-element work5">SANVT (ColorElephant)</div>
		<div class="work-element work6">Personal Training Project ()</div>
	</div>
</section>





<style>
	section {
		display: flex;
		flex-direction: column;
		justify-content: left;
		align-items: left;
		padding: 0 3rem;
	}
	
	.bg-cover {
		height: 100vh;
		width: 100vw;
		background-color: #ff6d1b;
		position: fixed;
		inset: 0px;
		z-index: 99;

		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		font-family: 'MontrealMedium';
		font-size: 68px;
	}
	
	.logo-name {
		font-family: 'MontrealBook';
		width: fit-content;
		padding: 0px 6px 0px 4px;
		border: 1px solid var(--color-text);
		border-radius: 12px;
	}
	.avatar {
		height: 100px;
		width: 100px;
		border-radius: 100px;
		background-color: #ff6d1b;
	}
	h1 {
		text-align: left;
	}

	.work-row {
		display: flex;
		flex-direction: row;
		gap: 24px;
		margin-top: 24px;
	}
	.work-element {
		height: 400px;
		border-radius: 20px;
		padding: 24px;
	}
	.work1 {
		flex-grow: 2;
		background-color: aqua;
	}
	.work2 {
		flex-grow: 1;
		background-color:beige;
	}
	.work3 {
		flex-grow: 1;
		background-color:cadetblue;
	}
	.work4 {
		flex-grow: 2;
		background-color:cornflowerblue
	}
	.work5 {
		flex-grow: 2;
		background-color:wheat;
	}
	.work6 {
		flex-grow: 1;
		background-color:cadetblue;
	}

	.hero-image {
		background-color: #ff6d1b;
		height: 620px;
		border-radius: 20px;
	}
</style>
