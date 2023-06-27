<script>
    import Header from "../Menu.svelte";
    import cover1 from '$lib/images/Card 1.jpg'
    import pulse1 from '$lib/images/pulse1.jpg'
    import pulse2 from '$lib/images/pulse2.jpg'
    import pulse3 from '$lib/images/pulse3.jpg'
    import pulse4 from '$lib/images/pulse4.jpg'
    import LineDivider from "$lib/icons/decor/LineDivider.svelte";
    import pulse from '$lib/icons/decor/pulse.svg'
    import Footer from "../../blocks/Footer.svelte";

</script>
<svelte:head>
	<title>ExpensePulse™</title>
	<meta name="description" content="About this app" />
</svelte:head>

<Header moveToBottom={true} />

<section>
    <img src={cover1} alt="" />
    <!-- <img src={pulse} alt="" style="width: 24px;" /> -->

        <div class="two-elements">
            <div class="title">ExpensePulse™</div>

            <div class="grid">
                <div class="grid-2">
                    <div class="info">
                        <div class="role">Role</div>
                        <div class="descr">Lead Product Designer</div>
                    </div>
                    <div class="info">
                        <div class="role">Responsibilities</div>
                        <div class="descr">Research, System Design, UI Design, UX Design, Prototyping</div>
                    </div>
                </div>

                    <div class="info">
                        <div class="role">Results</div>
                        <div class="descr">
                            <ul>
                                <li>Product successfully launched.</li>
                                <li>Table concept received great feedback and replaced old table’s UI in other company products.</li>
                                <li>Design system has continued its successful growth with the addition of new features.</li>
                            </ul>
                        </div>
                    </div>
            </div>               
        </div>

        <div class="content">
            <div class="title-2">The<br />challenge</div>
            <div class="body-text">
                <p>Private aviation often involves complex billing structures, such as fractional ownership, charter flights, or aircraft management agreements. Owners may utilize their aircraft for both personal and business purposes. Proper expense tracking enables them to differentiate between personal and business-related costs, facilitating accurate tax reporting and maximizing potential tax deductions.</p>
                <p>Therefore, private aviation segment requires a convenient way of logging expenses and accounting is crucial in private aviation to maintain financial control, facilitate accurate billing and invoicing, enable proper tax reporting, and ensure effective communication among various stakeholders involved in the operations.</p>
            </div>
        </div>

        <img class="cover" src={pulse1} alt="" height="100%">
        
        <img class="cover" src={pulse2} alt="">

        <img class="cover" src={pulse3} alt="">
        
        <img class="cover" src={pulse4} alt="">

  
</section>

<style>
    section {
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        font-family: 'MontrealMedium';
    }

    .two-elements {
        width: 100%;
        display: flex;
        gap: 48px;
        padding: 80px 48px;
        background: white;
    }
        .title {
            font-size: 32px;
            font-family: 'MontrealMedium';
            font-weight: 500;
            flex: 1;
        }
        .descr {
            font-size: 16px;
            line-height: 24px;
            letter-spacing: 0.32px;
            font-weight: 400;
            font-family: 'MontrealBook';
        }

        .grid {
                display: flex;
                flex-direction: column;
                gap: 48px;
                flex: 1;
                margin-right: 124px;
        }

        .info {
            display: flex;
            flex-direction: column;
            flex: 1;
            gap: 10px;
        }
            .grid-2 {
                display: flex;
                gap: 24px;
            }

            .role {
                font-size: 12px;
                letter-spacing: 1px;
                text-transform: uppercase;
                font-weight: 500;
                font-family: 'MontrealMedium';
            }

    ul {
        margin-block-start: 0;
        margin-block-end: 0;
        padding-inline-start: 16px;
        display: flex;
        flex-direction: column;
        gap: 10px;
    }
    li {
        line-height: 24px;
        font-size: 16px;
        letter-spacing: 0.32px;
        font-weight: 400;
        font-family: 'MontrealBook';
    }
    .content {
        display: flex;
        flex-direction: row;
        padding: 80px 48px;
        gap: 24px;
    }
    .title-2 {
        font-size: 62px;
        line-height: 62px;
        text-transform: uppercase;
        font-family: 'MontrealBook';
        font-weight: 400;
        flex: 1;
    }
    .body-text {
        display: flex;
        flex-direction: column;
        gap: 24px;
        flex: 1;
        margin-right: 124px;
    }
            
    p {
        font-size: 20px;
        line-height: 32px;
        letter-spacing: 0.4px;
        font-family: 'MontrealBook';
    }


    /* Info parts */

     /* Info parts */
    .cover {
        background: #BBD1F3;
        height: 500px;
        display: flex;
        flex: 1 0 auto;
        margin: 0px 48px 80px 48px;
        border-radius: 20px;

        /* pointer-events: none;
		user-select: none;
		object-position: center;
		object-fit: cover;
		image-rendering: auto; */

		z-index: -2;
		transition: transform 0.3s ease-in-out;
    }
    
</style>