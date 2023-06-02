<script>
	import welcome from '$lib/images/svelte-welcome.webp';
	import welcome_fallback from '$lib/images/svelte-welcome.png';

	import { animate } from "motion";
	import { onMount } from 'svelte';
	

	// onMount(() => {
	// 	animate(
	// 		".blink",
	// 		{ opacity: [1,0,1] },
  	// 		{ duration: 3, repeat: Infinity },
	// 		);

	// 	animate(
	// 		".bg-cover",
	// 		{ x: '-100vw' },
  	// 		{ duration: 0.5, delay: 1, allowWebkitAcceleration: true },
	// 		);	
	// });
	



</script>

<svelte:head>
	<title>Home</title>
	<meta name="description" content="Svelte demo app" />
</svelte:head>



<!-- 
<div class="bg-cover">Hello, I'm Ihor</div> -->

<section>

	<div class="main-info">
		<div class="name">
			<div class="top-text">
				<div class="tag">NAME <span class="ua-description">&nbsp⁄ ім’я</span></div>
				<div class="ua-description">ігор притуляк</div>
			</div>
			<div class="main-text">Ihor Prytuliak</div>
		</div>
		<div class="position">
			<div class="top-text">
				<div class="tag">ROLE <span class="ua-description">&nbsp⁄ роль</span></div>
				<div class="ua-description">дизайнер інтерфейсів</div>
			</div>
			<div class="main-text">Senior UX/UI Designer</div>
		</div>
		<div class="talk">
			<div class="top-text">
				<div class="ua-description">зв’язатись</div>
			</div>
			<div class="main-text">Talk</div>
		</div>
	</div>	



	<div class="hero-image"></div>

	<div class="work-row">
		<div class="work-element work1">ExpensePulse™ (Portside)</div>
		<div class="work-element work2">Staffing Marketplace (JetAviation/Portside)</div>
	</div>
	<div class="work-row">
		<div class="work-element work3">PAX App (Airshare/Portside)</div>
		<div class="work-element work4">FC Dynamo Kyiv (Linecore)</div>
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
	.main-info {
		margin-top: 19%;
		margin-bottom: 20%;
		display: flex;
		gap: 16px;
	}
	/* Main Info Cards */
	.name {
		background: #C2EF56;
		border-radius: 10px;
		padding: 14px 20px;
		width: 370px;
	}
	.position {
		background: #B9ACF2;
		border-radius: 10px;
		padding: 14px 20px;
		width: 685px;
	}
	.talk {
		border-radius: 10px;
		padding: 14px 20px;
		width: 190px;
		box-shadow: 0 0 0 3px rgba(0, 0, 0, 0.7);
	}
	.top-text {
		display: flex;
		justify-content: space-between;
	}
	.ua-description {
		font-weight: 400;
		opacity: 0.5;
		font-family: 'MontrealBook';
	}
	.tag {
		font-family: 'MontrealMedium';
		font-size: 16px;
		font-weight: 500;
		line-height: 19px;
		letter-spacing: 0em;
		text-align: left;
		color: rgba(0, 0, 0, 0.7);
	}
	.main-text {
		font-family: 'MontrealMedium';
		font-size: 68px;
		font-weight: 500;
		line-height: 68px;
		letter-spacing: -0.02em;
		text-align: left;
		color: rgba(0, 0, 0, 0.7);

	}
	/* Main Info Cards */



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
		background: linear-gradient(to bottom right, #ff9a9e, #fad0c4);
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
