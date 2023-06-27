<div class="footer">
    <div class="socials cl-effect-5">
        <a href="#"><span data-hover="Twitter ↗">Twitter ↗</span></a>
        
        <a href="#"><span data-hover="LinkedIn ↗">LinkedIn ↗</span></a>
        <a href="#"><span data-hover="Instagram ↗">Instagram ↗</span></a>
        <a href="#"><span data-hover="Dribbble ↗">Dribbble ↗</span></a>
    </div>
</div>

<style>
    .footer {
        display: flex;
        justify-content: center;
        height: 128px;
        width: 100%;
        margin-top: 96px;
        margin-bottom: 48px;
    }
    .socials {
        width: 100%;
        display: flex;
        justify-content: space-between;
    }
    a { 
        color: var(--color-text);
        font-size: 32px;
        font-family: 'MontrealMedium';
    }

    /* Effect 5: same word slide in */
    .cl-effect-5 a {
        overflow: hidden;
        padding: 0 4px;
        height: 1.2em;
    }

    .cl-effect-5 a span {
        position: relative;
        display: inline-block;
        -webkit-transition: -webkit-transform 0.3s;
        -moz-transition: -moz-transform 0.3s;
        transition: transform 0.3s;
    }

    .cl-effect-5 a span::before {
        position: absolute;
        top: 100%;
        content: attr(data-hover);
        /* font-weight: 700; */
        -webkit-transform: translate3d(0,0,0);
        -moz-transform: translate3d(0,0,0);
        transform: translate3d(0,0,0);
    }

    .cl-effect-5 a:hover span,
    .cl-effect-5 a:focus span {
        -webkit-transform: translateY(-100%);
        -moz-transform: translateY(-100%);
        transform: translateY(-100%);
    }
</style>