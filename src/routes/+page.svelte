<script>

    import FeaturedClients from '../blocks/FeaturedClients.svelte';
    import MainInfo from '../blocks/MainInfo.svelte';
    import ExpensePulse from '../blocks/ProjectCards/ExpensePulse.svelte';
    import StaffingMarketplace from '../blocks/ProjectCards/StaffingMarketplace.svelte';
    import Header from './Header.svelte';
	

</script>

<svelte:head>
	<title>Home</title>
	<meta name="description" content="Svelte demo app" />
</svelte:head>



<!-- 
<div class="bg-cover">Hello, I'm Ihor</div> -->

<section id="main">

	<MainInfo />

	<div class="bottom">
		<Header />
		<a href="#portfolio">
			<div class="work">Work ↓</div>
		</a>
	</div>

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
	
	/* .bg-cover {
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
	} */
	.bottom {
		display: flex;
		justify-content: space-between;
		margin-bottom: 32px;
		margin-top: -175px;
	}
	.work {
		font-family: 'MontrealMedium';
		font-size: 128px;
		height: 128px;
		background: linear-gradient(to right, #000 0%, #383449 35%, #E56A26 100%);
		-webkit-background-clip: text;
		-webkit-text-fill-color: transparent;
		transition: 0.3s;
	}
	.work:hover {
		background: linear-gradient(to right, #E56A26 0%, #E56A26 100%);
		-webkit-background-clip: text;
		-webkit-text-fill-color: transparent;
	}
	.work-row {
		display: flex;
		flex-direction: column;
		width: 100%;
		gap: 48px;
		margin-top: 24px;
	}
	a {
		text-decoration: none;
	}
</style>
