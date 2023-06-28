<script>

    import FeaturedClients from '../blocks/FeaturedClients.svelte';
    import MainInfo from '../blocks/MainInfo.svelte';
    import Card from '../blocks/ProjectCards/Card.svelte';
    import Header from './Menu.svelte';
	import cover1 from '$lib/images/Card 1.jpg'
	import cover2 from '$lib/images/Card 2.jpg'
	import cover3 from '$lib/images/Card 3.jpg'
	import cover4 from '$lib/images/Card 4.jpg'
	import cover5 from '$lib/images/Card 5.jpg'
	import cover6 from '$lib/images/Card 6.jpg'
	import pulse from '$lib/icons/decor/pulse.svg'
	import marketplace from '$lib/icons/decor/marketplace.svg'
	import fc from '$lib/icons/decor/fc.svg'
	import pax from '$lib/icons/decor/pax.svg'
	import sanvt from '$lib/icons/decor/sanvt.svg'
	import x from '$lib/icons/decor/x.svg'
	import glass from '$lib/images/glass.jpeg'

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

	<!-- <iframe src='https://my.spline.design/glassspheres-babee2be1ebcecb767457ea34f7f5e5a/' frameborder='0' width='100%' height='100%'></iframe> -->
	<!-- <video autoplay loop width="100%" height='100%'>
		<source src={video} type="video/mp4">
	</video> -->
	<img src={glass} alt="" width="100%" height='100%'>


	<div class="work-row" id="portfolio">
		<Card
			link="/pulse"
			cover={cover1}
			icon={pulse}
			title="ExpensePulse™"
			description="Changing the way business aviation trip expenses are compiled, audited, and reported."
		 />
		
		 <Card
			cover={cover2}
			icon={marketplace}
			title="Staffing Marketplace™"
			description="Connecting job seekers and employers for full-time and part-time opportunities as well as temporary assignments."
			whiteText={true}
		 />

		 <Card
		 cover={cover3}
		 icon={fc}
		 title="FC Dynamo Kyiv"
		 description="Connecting job seekers and employers for full-time and part-time opportunities as well as temporary assignments."
	 	 />

		 <FeaturedClients />

		 <Card
		 cover={cover4}
		 icon={pax}
		 title="PAX App"
		 description="High-performance optimization and management tool designed to enable seamless communication between crew and staff members, increase visibility into schedule and save costs on crew bookings."
	 	 />

		<Card
		cover={cover5}
		icon={sanvt}
		title="SANVT"
		description="Connecting job seekers and employers for full-time and part-time opportunities as well as temporary assignments."
		/>

		<Card
		cover={cover6}
		icon={x}
		title="Personal Training Project X"
		description="Connecting job seekers and employers for full-time and part-time opportunities as well as temporary assignments."
		/>
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
	
	.work-row {
		display: flex;
		flex-direction: column;
		width: 100%;
		gap: 48px;
		padding-top: 48px;
		margin-top: -90px;
	}
	img {
		position: absolute;
		z-index: 0;
		left:-170px;
		bottom: 40px;
		opacity: 0;
		animation: fade 3s forwards;
		object-fit: cover;
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
