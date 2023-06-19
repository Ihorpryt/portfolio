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
		gsap.from(".talk-animation", { opacity: 0, width:0, duration: 1, delay:2});
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
	<a href="#">
		<div class="talk talk-animation">
			<div class="top-text">
				<div class="ua-description">зв’язатись</div>
			</div>
			<div class="main-text">Talk<span class="blink">
				<svg width="19" height="19" viewBox="0 0 19 19" fill="none" xmlns="http://www.w3.org/2000/svg">
					<path class="message" d="M0 18.4603V9.5012C0 4.17972 4.37161 -0.116331 9.72547 0.00240326C14.7771 0.121138 18.9004 4.25527 18.9976 9.30691C19.0516 12.0054 17.9722 14.4557 16.2127 16.2151C14.4965 17.9314 12.1218 19 9.4988 19H0.539704C0.248264 19 0 18.7517 0 18.4603Z" />
				</svg>
			</span></div>
		</div>
	</a>
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
		width: 370px;
		overflow: hidden;
		white-space: nowrap;
	}
	.position {
		background: #B9ACF2;
		border-radius: 10px;
		padding: 14px 20px;
		width: 650px;
		overflow: hidden;
		white-space: nowrap;
	}
	.talk {
		border-radius: 10px;
		padding: 14px 20px;
		width: 150px;
		box-shadow: 0 0 0 3px rgba(0, 0, 0, 0.7);
		transition: background-color 0.3s;
		overflow: hidden;
		white-space: nowrap;
	}
	.message {
		fill: #47484A;
	}
	.talk:hover {
		background-color:rgba(0, 0, 0, 0.7);
		color: white;
	}
	.talk:hover .ua-description {
		color: white;
		opacity: 1;
	}
	.talk:hover .main-text {
		color: white;
	}
	.talk:hover .message {
		fill: white;
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
</style>
