<script>

	export let cover;
	export let title;
	export let description;
</script>
<a href="#">
	<div class="work-element">
		<div class="info">
			<svg width="24" height="24" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
				<path fill-rule="evenodd" clip-rule="evenodd" d="M7.68012 0H23.8801V16.2H22.8236V8.1C22.8236 4.21 19.6702 1.05652 15.7801 1.05652C11.8901 1.05652 8.73664 4.20998 8.73664 8.1V16.2H7.68012V0ZM16.3201 7.8V24H0.120117L0.120118 7.8H1.17664V15.9C1.17664 19.79 4.33011 22.9435 8.22012 22.9435C12.1102 22.9435 15.2636 19.79 15.2636 15.9V7.8H16.3201Z" fill="black"/>
			</svg>
			<div class="title">{title}</div>
			<div class="description"> {description} </div>
		</div>
		<img src={cover} alt="">
	</div>
</a>


<style>
    .work-element {
		display: flex;
		align-items: flex-end;
		min-height: 420px;
		border-radius: 20px;
        /* background-color: #F2C04B; */
        flex: 1;
		opacity: 0;
		animation: fade 1s forwards; 
		animation-delay: 3.5s;
		overflow: hidden;
	}
	.work-element:hover img {
		transform: scale(1.15);
		/* opacity: 0.2; */
	}
	@keyframes fade {
		0% {
			opacity: 0;
		}
		100% {
			opacity: 1;
		}
	}
	.info {
		position: absolute;
		display: flex;
		flex-direction: column;
		gap: 12px;
		width: 300px;
		margin-left: 48px;
		margin-bottom: 48px;
	}
	.title {
		color: var(--color-text);
		font-family: 'MontrealMedium';
		font-size: 24px;
	}
	.description {
		color: var(--color-text);
		font-size: 16px;
		font-family: 'MontrealBook';
		line-height: 20px;
		letter-spacing: 0.03em;
	}
	img {
		pointer-events: none;
		user-select: none;
		display: block;
		width: 100%;
		height: 100%;
		border-radius: inherit;
		object-position: center;
		object-fit: cover;
		image-rendering: auto;

		z-index: -2;
		transition: transform 0.3s ease-in-out;
	}
</style>