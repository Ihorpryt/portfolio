<script>
    import Header from "../Menu.svelte";
    import cover1 from '$lib/images/Card 1.jpg'
    import pulse1 from '$lib/images/pulse1.jpg'
    import pulse2 from '$lib/images/pulse2.jpg'
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
    <img src={cover1} alt="">
    <div class="content">
        <div class="copy">
            <img src={pulse} alt="" style="width: 24px;" />
            <div class="title">ExpensePulse™ • 2022</div>

            <div class="details-2">
                <div class="additional-info">
                    <div class="info-type">ROLE</div>
                    <div class="info">Lead Product Designer</div>
                </div>
                <div class="additional-info padding">
                    <div class="info-type">Responsibilities</div>
                    <div class="info">Research, System Design, UI Design, UX Design, Prototyping</div>
                </div>
            </div>

            <div class="additional-info">
                <div class="info-type">Results</div>
                <ul>
                    <li>Product successfully launched. </li>
                    <li>Table concept received great feedback and replaced old table’s UI in other company products. </li>
                    <li>Design system has continued its successful growth with the addition of new features.</li>
                </ul> 
            </div>

            <LineDivider />

            <h3>The Challenge</h3>
            <p>Private aviation often involves complex billing structures, such as fractional ownership, charter flights, or aircraft management agreements. Owners may utilize their aircraft for both personal and business purposes. Proper expense tracking enables them to differentiate between personal and business-related costs, facilitating accurate tax reporting and maximizing potential tax deductions.</p>
            <p>Therefore, private aviation segment requires a convenient way of logging expenses and accounting is crucial in private aviation to maintain financial control, facilitate accurate billing and invoicing, enable proper tax reporting, and ensure effective communication among various stakeholders involved in the operations.</p>
        </div>

        <img class="showcase cover" src={pulse1} alt="" height="100%">
        
        <div class="copy">
            <LineDivider />
            <h3>Research & Findings</h3>
            <h4>Modern Grid</h4>
            <p>There will be multiple records of different kinds and parameters. The table was chosen as the best option for displaying such types of information as transactions, invoices, and others. In addition, I had the opportunity not to use the existing interface of the table from other products of the company that existed at that time.</p>
            <p>For reference, I took Airtable, Google Sheets and web version of Microsoft Excel. After review of those products I decided to implement most notable things like:</p>
            <ul class="in-content">
                <li>Height of the cells and rows to incorporate as much information to the viewport as possible.</li>
                <li>Give table the full width of viewport.</li>
                <li>Ability to edit inline where it’s needed which would speed up process of making necessary changes to data.</li>
                <li>Add ability to resize columns.</li>
                <li>Different types of users have different priorities and ability to change order of the columns as well as ability to turn on/off some of them (to remove unnecessary distractions), will be crucial for modern workflows.</li>
            </ul> 
        </div>

        <img class="showcase cover" src={pulse2} alt="">

        <div class="copy">
            <h4>Displaying & Editing</h4>
            <p>In order to minimize any potential issues with information overload, it is essential to strategically place accents and other visual cues to help guide the user's attention. Additionally, inline editing can be a powerful tool for users who need to make quick adjustments to their work, as it allows them to make changes right where they need them without having to navigate away from their current location within the document.</p>
        </div>

        <img class="showcase cover" src={pulse1} alt="">

        <div class="copy">
            <h4>Customization</h4>
            <p>In some cases, it will be important to match information with an event or one type of information with a completely different type of information. Also, these priorities can change quite dynamically. For this, the ability to change the size of different sections on one screen was implemented. The function of switching certain sections within a group has also been added.</p>
            <p>These changes are saved in a similar way to user-modified tables. When a user saves a product with their specific needs, they can view a unique version of the product. In addition, you have the ability to customize the background color of the product, so it can match the user's mood or adhere to the guidelines of their brand. Furthermore, these customizations allow your users to feel more connected to your product and give them a sense of personalization and ownership.</p>
        </div>
        
        <img class="showcase cover" src={pulse1} alt="">

        <div class="copy">
            <LineDivider />
            <h3>Summary</h3>
            <p>Building a strong foundation of core concepts is essential for the success of any development project. When it comes to design, having a solid understanding of the underlying principles is crucial to creating an efficient and effective product. This is where design systems come into play. By providing a unified framework for design, a design system allows teams to work together seamlessly and build new features that align with the product vision. With a design system in place, designers can be confident that their work is not only visually consistent but also meets the needs of the user and the business. This results in a better user experience and ultimately drives the success of the product.</p>
        </div>

        <Footer />

    </div>    
</section>

<style>
    section {
        width: 100%;
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        font-family: 'MontrealMedium';
    }
    img {
        width: 100%;
        height: 100%;
    }
    .content {
        display: flex;
        flex-direction: column;
        align-items: center;
        padding: 80px 48px;
    }
    .copy {
        width: 680px;
        display: flex;
        flex-direction: column;
        gap: 24px;
    }
    .title {
        font-size: 48px;
        font-family: 'MontrealMedium';
    }
    .padding {
        padding-left: 24px;
        border-left: 1px solid black;
    }
    .details-2 {
        display: flex;
        flex-direction: row;
        margin-top: 36px;
    }

    h3 {
            font-size: 32px;
            line-height: 32px;
            text-transform: uppercase;
            font-family: 'MontrealMedium';
    }
    p {
        font-size: 20px;
        line-height: 32px;
        letter-spacing: 0.4px;
        font-family: 'MontrealMedium';
    }

    ul {
        padding-inline-start: 14px;
        margin-block-start: 0px;
    }
    li {
        margin-bottom: 4px;
    }
    .in-content li {
        font-size: 20px;
        line-height: 32px;
        letter-spacing: 0.4px;
        font-family: 'MontrealMedium';
        margin-bottom: 12px;
    }
    /* Info parts */

    .additional-info {
        display: flex;
        flex-direction: column;
        gap: 10px;
        flex: 1 0 0;
    }
    .info-type {
        font-size: 12px;
        letter-spacing: 1.56px;
        text-transform: uppercase;
    }
    .info {
        font-size: 16px;
        line-height: 24px;
        letter-spacing: 0.32px;
    }
     /* Info parts */
    .showcase {
        background: #BBD1F3;
        height: 500px;
        display: flex;
        flex: 1 0 auto;
        margin: 80px 0px;
        border-radius: 20px;
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