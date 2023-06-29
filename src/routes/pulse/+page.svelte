<script>
    import Header from "../Menu.svelte";
    import cover1 from '$lib/images/Card 1.jpg'
    import pulse1 from '$lib/images/pulse1.jpg'
    import pulse2 from '$lib/images/pulse2.jpg'
    import pulse3 from '$lib/images/pulse3.jpg'
    import pulse4 from '$lib/images/pulse4.jpg'
    import LineDivider from "$lib/icons/decor/LineDivider.svelte";
    import pulse from '$lib/icons/decor/pulse.svg'

</script>
<svelte:head>
	<title>ExpensePulse™</title>
	<meta name="description" content="About this app" />
</svelte:head>

<Header moveToBottom={true} />

<section>
    <img src={cover1} class="top-image" alt="" />
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

        <div class="content-spread">
            <div class="title-2">The<br />challenge</div>
            <div class="body-text">
                <p>Private aviation often involves complex billing structures, such as fractional ownership, charter flights, or aircraft management agreements. Owners may utilize their aircraft for both personal and business purposes. Proper expense tracking enables them to differentiate between personal and business-related costs, facilitating accurate tax reporting and maximizing potential tax deductions.</p>
                <p>Therefore, private aviation segment requires a convenient way of logging expenses and accounting is crucial in private aviation to maintain financial control, facilitate accurate billing and invoicing, enable proper tax reporting, and ensure effective communication among various stakeholders involved in the operations.</p>
            </div>
        </div>

        <img class="cover" src={pulse1} alt="" height="100%">

        <div class="content-spread">
            <div class="title-2">Research &<br />Findings</div>
            <div class="body-text">
                <h4>Modern Grid</h4>
                <p>There will be multiple records of different kinds and parameters. The table was chosen as the best option for displaying such types of information as transactions, invoices, and others. In addition, I had the opportunity not to use the existing interface of the table from other products of the company that existed at that time.</p>
                <p>For reference, I took Airtable, Google Sheets and web version of Microsoft Excel. After review of those products I decided to implement most notable things like:</p>
                <ul>
                    <li class="list-inside-text">Height of the cells and rows to incorporate as much information to the viewport as possible.</li>
                    <li class="list-inside-text">Give table the full width of viewport.</li>
                    <li class="list-inside-text">Ability to edit inline where it’s needed which would speed up process of making necessary changes to data.</li>
                    <li class="list-inside-text">Add ability to resize columns.</li>
                    <li class="list-inside-text">Different types of users have different priorities and ability to change order of the columns as well as ability to turn on/off some of them (to remove unnecessary distractions), will be crucial for modern workflows.</li>
                </ul>
            </div>
        </div>
        
        <img class="cover" src={pulse2} alt="">

        <div class="content-center">
            <h4>Displaying & Editing</h4>
            <div class="body-text">
                <p>In order to minimize any potential issues with information overload, it is essential to strategically place accents and other visual cues to help guide the user's attention. Additionally, inline editing can be a powerful tool for users who need to make quick adjustments to their work, as it allows them to make changes right where they need them without having to navigate away from their current location within the document.</p>
            </div>
        </div>

        <img class="cover" src={pulse3} alt="">

        <div class="content-center">
            <h4>Customization</h4>
            <div class="body-text">
                <p>In some cases, it will be important to match information with an event or one type of information with a completely different type of information. Also, these priorities can change quite dynamically. For this, the ability to change the size of different sections on one screen was implemented. The function of switching certain sections within a group has also been added.</p>
                <p>These changes are saved in a similar way to user-modified tables. When a user saves a product with their specific needs, they can view a unique version of the product. In addition, you have the ability to customize the background color of the product, so it can match the user's mood or adhere to the guidelines of their brand. Furthermore, these customizations allow your users to feel more connected to your product and give them a sense of personalization and ownership.</p>
            </div>
        </div>
        
        <img class="cover" src={pulse4} alt="">

        <div class="content-spread">
            <div class="title-2">Summary</div>
            <div class="body-text">
                <p>Building a strong foundation of core concepts is essential for the success of any development project. When it comes to design, having a solid understanding of the underlying principles is crucial to creating an efficient and effective product. This is where design systems come into play. By providing a unified framework for design, a design system allows teams to work together seamlessly and build new features that align with the product vision. With a design system in place, designers can be confident that their work is not only visually consistent but also meets the needs of the user and the business. This results in a better user experience and ultimately drives the success of the product.</p>
            </div>
        </div>
 
</section>


<style>
    section {
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        font-family: 'MontrealMedium';
    }
    .top-image {
        width: 100%;
        height: 100%;
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
    .list-inside-text {
        font-size: 20px;
        line-height: 32px;
        letter-spacing: 0.4px;
    }
    .content-spread {
        display: flex;
        flex-direction: row;
        padding: 80px 48px;
        gap: 24px;
    }
    .content-center {
        display: flex;
        flex-direction: column;
        padding: 80px 48px;
        gap: 24px;
        width: 680px;
    }
    .content-center .body-text {
        margin-right: 0;
    }
    .title-2 {
        font-size: 62px;
        line-height: 62px;
        text-transform: uppercase;
        font-family: 'MontrealBook';
        font-weight: 400;
        flex: 1;
    }
    h4 {
        font-family: 'MontrealBook';
        font-weight: 400;
        font-size: 24px;
        line-height: 32px;
        letter-spacing: 0.4px;
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
        margin: 0px 48px 0px 48px;
        border-radius: 20px;

        /* pointer-events: none;
		user-select: none;
		object-position: center;
		object-fit: cover;
		image-rendering: auto; */

		z-index: -2;
		transition: transform 0.3s ease-in-out;
    }


    @media (max-width: 480px) {
		section {
			overflow: hidden;
            width: 100%;
		}
        .content-spread {
            flex-direction: column;
        }
        .body-text {
            margin-right: 0;
        }
        .two-elements {
            flex-direction: column;
        }
        .grid {
            margin-right: 0;
        }
        .cover {
            width: 100%;
        }
	} 
    
</style>