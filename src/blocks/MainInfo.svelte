<script>
	// import welcome from '$lib/images/svelte-welcome.webp';
	// import welcome_fallback from '$lib/images/svelte-welcome.png';
	import src from '$lib/images/avatar.png'
	import {onMount} from 'svelte';

	import { animate } from "motion";
	import {gsap} from "gsap";

	// import { onMount } from 'svelte';
    import Message from '$lib/icons/Message.svelte';
    import Vector1 from '$lib/icons/Vector 1.svelte';
    import Vector2 from '$lib/icons/Vector 2.svelte';
    import Talk from './Talk.svelte';

	

	onMount(() => {
		// animate(
		// 	".blink",
		// 	{ opacity: [1,0,1] },
  		// 	{ duration: 3, repeat: Infinity },
		// 	);

		// animate(
		// 	".bg-cover",
		// 	{ x: '-100vw' },
  		// 	{ duration: 0.5, delay: 1, allowWebkitAcceleration: true },
		// 	);

		gsap.to(".main-info", { opacity: 1, duration: 0.5});
		gsap.from(".avatar", { keyframes: {opacity: [0,1,0,1,0,1]}, duration: 1});
		gsap.from(".name", { opacity: 0, width:0, duration: 1, delay:0.5});
		gsap.from(".vector", { opacity: 0, duration: 1, delay:1});
		gsap.from(".position", { opacity: 0, width:0, duration: 1, delay:1.5});
		// gsap.from(".talk-animation", { opacity: 0, width:0, duration: 1, delay:2});
	});


</script>

<div class="main-info">
	<img {src} alt="avatar" class="avatar" >

    <div class="name">
        <div class="top-text">
            <div class="tag">NAME <span class="ua-description">&nbsp⁄ ім’я</span></div>
            <div class="ua-description">ігор притуляк</div>
        </div>
        <div class="main-text">Ihor Prytuliak</div>
    </div>

	<div class="vector">
    <Vector1 />
	</div>

    <div class="position">
        <div class="top-text">
            <div class="tag">ROLE <span class="ua-description">&nbsp⁄ роль</span></div>
            <div class="ua-description">дизайнер інтерфейсів</div>
        </div>
        <div class="main-text">Senior UX/UI Designer</div>
        <!-- <div class="add-info">USER EXPERIENCE &nbsp⁄&nbsp USER INTERFACE</div> -->
    </div>
    <!-- <Vector2 /> -->
	<Talk />
</div>	


<style>
	img {
        height: 115px;
    }
	.main-info {
		margin-top: 19%;
		margin-bottom: 23%;
		display: flex;
		gap: 16px;
		width: 100%;
		opacity: 0;
		z-index: 3;
	}
	.name {
		background: #C2EF56;
		border-radius: 10px;
		padding: 14px 20px;
		width: fit-content;
		overflow: hidden;
		white-space: nowrap;
	}
	.position {
		background: #B9ACF2;
		border-radius: 10px;
		padding: 14px 20px;
		width: fit-content;
		overflow: hidden;
		white-space: nowrap;
	}
	.top-text {
		display: flex;
		justify-content: space-between;
	}
	.tag {
		font-family: 'MontrealMedium';
		font-size: 16px;
		line-height: 19px;
		text-align: left;
		color:var(--color-text);
		-webkit-font-smoothing: antialiased;
	}
	.ua-description {
		color:var(--color-text);
		opacity: 0.5;
		font-family: 'MontrealBook';
		-webkit-font-smoothing: antialiased;
	}
	.main-text {
		font-family: 'MontrealMedium';
		font-size: 68px;
		line-height: 68px;
		letter-spacing: -0.02em;
		text-align: left;
		color:var(--color-text);
		-webkit-font-smoothing: antialiased;

	}
	.add-info {
		position: absolute;
		margin-top: 30px;
		margin-left: 8px;
		font-family: 'MontrealBook';
		letter-spacing: 0.84em;
		text-transform: uppercase;
		font-size: 14px;
		line-height: 17px;
		-webkit-font-smoothing: antialiased;
	}
	.blink {
		position: absolute;
    	margin-top: -38px;
	}
	a {
		text-decoration: none;
	}
	.vector {
		opacity: 1;
	}

	@media (max-width: 480px) {
		.main-info {
			flex-wrap: wrap;
		}
	} 
</style>
