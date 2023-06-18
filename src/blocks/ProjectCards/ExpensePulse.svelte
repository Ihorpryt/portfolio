<script>
	import cover from '$lib/images/Card 2.jpg'
</script>

<div class="work-element">
	<div class="info">
		<svg width="24" height="24" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
			<path fill-rule="evenodd" clip-rule="evenodd" d="M7.68012 0H23.8801V16.2H22.8236V8.1C22.8236 4.21 19.6702 1.05652 15.7801 1.05652C11.8901 1.05652 8.73664 4.20998 8.73664 8.1V16.2H7.68012V0ZM16.3201 7.8V24H0.120117L0.120118 7.8H1.17664V15.9C1.17664 19.79 4.33011 22.9435 8.22012 22.9435C12.1102 22.9435 15.2636 19.79 15.2636 15.9V7.8H16.3201Z" fill="black"/>
		</svg>
		<div class="title">ExpensePulse™</div>
		<div class="description">Changing the way business aviation trip expenses are compiled, audited, and reported.</div>
	</div>
	<img src={cover} alt="">
</div>


<style>
    .work-element {
		display: flex;
		align-items: flex-end;
		min-height: 420px;
		border-radius: 20px;
        background-color: #F2C04B;
        flex: 1;
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
	}
</style>