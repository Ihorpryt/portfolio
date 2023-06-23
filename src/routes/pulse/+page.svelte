<script>
    import Header from "../Menu.svelte";
    import cover1 from '$lib/images/Card 1.jpg'

</script>
<svelte:head>
	<title>ExpensePulseTM</title>
	<meta name="description" content="About this app" />
</svelte:head>

<Header />

<section>
    <img src={cover1} alt="">
    <div class="copy">
        <div class="title">ExpensePulseTM - 2022</div>
        <div class="text-block">Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.</div>
        <div class="additional-info">
            <div class="info-type">ROLE</div>
            <div class="info">Designer</div>
        </div>
    </div>
</section>

<style>
    section {
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
    }
    img {
        width: 100%;
        height: 100%;
    }
    .copy {
        margin-top: 50px;
        width: 50%;
    }
    .title {
        font-size: 24px;
    }
    .text-block {
        margin-top: 24px;
        font-size: 16px;
    }

    /* Info parts */

    .additional-info {
        display: flex;
        flex-direction: column;
        margin-top: 12px;
    }
    .info-type {
        font-size: 12px;
    }
    .info {
        font-size: 16px;
    }
</style>