<script>
    import Star from "$lib/icons/decor/Star.svelte";
    import Airshare from "$lib/icons/logos/Airshare.svelte";
    import ColorElephant from "$lib/icons/logos/ColorElephant.svelte";
    import Dynamo from "$lib/icons/logos/Dynamo.svelte";
    import JetAviation from "$lib/icons/logos/JetAviation.svelte";
    import Portside from "$lib/icons/logos/Portside.svelte";
    import Sanvt from "$lib/icons/logos/Sanvt.svelte";

</script>
<section>
    <div class="tag">FEATURED CLIENTS <span class="ua-description">&nbsp⁄ клієнти</span></div>
    <div class="logos"> 

        <div class="logo"><Portside /></div> 
        <Star/>
        <div class="logo"><Airshare /></div>
        <Star/>
        <div class="logo"><ColorElephant/></div>  
        <Star/>
        <div class="logo"><JetAviation /></div> 
        <Star/>
        <div class="logo" style="margin-bottom: 10px;"><Dynamo /></div>
        <Star/> 
        <div class="logo"><Sanvt /> </div> 

    </div>
</section>

<style>

    section {
        display: flex;
		flex-direction: column;
		/* justify-content: center; */
        align-items: center;
        margin-top: 48px;
    }
    .logos {
        display: flex;
        flex-direction: row;
        width: 100%;
        opacity: 0.5;
        height: 115px;
        justify-content: center;
        align-items: center;
    }
    .logo {
        display: flex;
        justify-content: center;
        align-items: center;
        width: 100%;
        height: 115px;
    }
    .tag {
		font-family: 'MontrealMedium';
		font-size: 16px;
		line-height: 19px;
		color:var(--color-text);
        margin-left: 60px;
		-webkit-font-smoothing: antialiased;
	}
	.ua-description {
		opacity: 0.5;
		font-family: 'MontrealBook';
		-webkit-font-smoothing: antialiased;
	}
</style>