<script>

	export let cover;
	export let title;
	export let description;
	export let whiteText = false;
	export let icon;
	export let link;
</script>
<a href={link}>
	<div class="work-element">
		<div class="info">
			<img src={icon} alt="" style="width: 24px;" />
			<div class="title" class:white={whiteText}>{title}</div>
			<div class="description" class:white={whiteText}> {description} </div>
		</div>
		<img class="cover" src={cover} alt="">
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
		animation-delay: 3s;
		overflow: hidden;
	}
	.work-element:hover .cover {
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
		/* gap: 12px; */
		width: 300px;
		margin-left: 48px;
		margin-bottom: 48px;
	}
	.title {
		margin-top: 12px;
		margin-bottom: 4px;
		color: var(--color-text);
		font-family: 'MontrealMedium';
		font-size: 24px;
	}
	.description {
		color: var(--color-text);
		font-size: 16px;
		font-family: 'MontrealMedium';
		line-height: 20px;
		opacity: 0.7;
		transition: color 0.3s ease-in-out;
		/* letter-spacing: 0.03em; */
	}
	.white {
		color: rgba(255, 255, 255, 0.7)
	}
	.cover {
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