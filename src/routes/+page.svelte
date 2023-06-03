<script>

    import FeaturedClients from '../blocks/FeaturedClients.svelte';
import HeroImage from '../blocks/HeroImage.svelte';
    import MainInfo from '../blocks/MainInfo.svelte';
    import ExpensePulse from '../blocks/ProjectCards/ExpensePulse.svelte';
    import StaffingMarketplace from '../blocks/ProjectCards/StaffingMarketplace.svelte';
	

</script>

<svelte:head>
	<title>Home</title>
	<meta name="description" content="Svelte demo app" />
</svelte:head>



<!-- 
<div class="bg-cover">Hello, I'm Ihor</div> -->

<section>

	<MainInfo />

	<div class="work">Work ↓</div>

	<HeroImage />
	<FeaturedClients />

	<div class="work-row">
		<ExpensePulse />
		<StaffingMarketplace />
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

	.work {
		font-family: 'MontrealMedium';
		font-size: 128px;
		height: 128px;
		position: absolute;
		bottom: 82px;
		right: 48px;
		background: linear-gradient(to right, #383449 0%, #383449 35%, #E56A26 100%);;
		-webkit-background-clip: text;
		-webkit-text-fill-color: transparent;
	}
	.work-row {
		display: flex;
		flex-direction: row;
		width: 100%;
		gap: 24px;
		margin-top: 24px;
	}
</style>
