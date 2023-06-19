<script>

    import FeaturedClients from '../blocks/FeaturedClients.svelte';
    import MainInfo from '../blocks/MainInfo.svelte';
    import ExpensePulse from '../blocks/ProjectCards/ExpensePulse.svelte';
    import StaffingMarketplace from '../blocks/ProjectCards/StaffingMarketplace.svelte';
    import Header from './Menu.svelte';
	

</script>

<svelte:head>
	<title>Home</title>
	<meta name="description" content="Svelte demo app" />
</svelte:head>



<!-- 
<div class="bg-cover">Hello, I'm Ihor</div> -->

<section id="main">

	<Header />

	<MainInfo />

	<iframe src='https://my.spline.design/glassspheres-babee2be1ebcecb767457ea34f7f5e5a/' frameborder='0' width='100%' height='100%'></iframe>


	<div class="work-row" id="portfolio">
		<ExpensePulse />
		<StaffingMarketplace />
		<FeaturedClients />
		<ExpensePulse />
		<ExpensePulse />
		<ExpensePulse />
	</div>
	<!-- <div class="work-row">
		<div class="work-element work3">PAX App (Airshare/Portside)</div>
		<div class="work-element work4">FC Dynamo Kyiv (Linecore)</div>
	</div>
	<div class="work-row">
		<div class="work-element work5">SANVT (ColorElephant)</div>
		<div class="work-element work6">Personal Training Project ()</div>
	</div> -->
</section>





<style>
	section {
		display: flex;
		flex-direction: column;
		justify-content: left;
		align-items: left;
		padding: 0 3rem;
	}
	
	.work-row {
		display: flex;
		flex-direction: column;
		width: 100%;
		gap: 48px;
		padding-top: 48px;
		margin-top: -90px;
	}
	iframe {
		position: absolute;
		z-index: 0;
		left:-170px;
		bottom: 40px;
		opacity: 0;
		animation: fade 3s forwards;
	}
	@keyframes fade {
		0% {
			opacity: 0;
		}
		50% {
			opacity: 0;
		}
		100% {
			opacity: 1;
		}
	}

</style>
