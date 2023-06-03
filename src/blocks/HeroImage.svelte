<div class="hero-image">
    <div class="part part1"></div>
    <div class="part part2"></div>
    <div class="part part3"></div>
    <div class="part part4"></div>
</div>

<style>
    .hero-image {
		background: rgba(103, 103, 103, 1);
		height: 620px;
		border-radius: 20px;
		display: flex;
		flex-direction: row;
		overflow: hidden;
	}
	.part {
		display: flex;
		flex-grow: 1;
	}
	.part1 {
		background: rgba(103, 103, 103, 1);
	}
	.part2 {
		background: #515151;
	}
	.part3 {
		background: #C2EF56;
	}
	.part4 {
		background: radial-gradient(75.32% 75.32% at 50% 0%, #000000 0%, rgba(0, 0, 0, 0) 100%), #E56A26;
	}
</style>