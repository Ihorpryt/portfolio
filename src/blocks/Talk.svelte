<a href="#">
    <div class="talk talk-animation">
        <div class="top-text">
            <div class="ua-description">зв’язатись</div>
        </div>
        <div class="main-text">Talk<span class="blink">
            <svg width="19" height="19" viewBox="0 0 19 19" fill="none" xmlns="http://www.w3.org/2000/svg">
                <path class="message" d="M0 18.4603V9.5012C0 4.17972 4.37161 -0.116331 9.72547 0.00240326C14.7771 0.121138 18.9004 4.25527 18.9976 9.30691C19.0516 12.0054 17.9722 14.4557 16.2127 16.2151C14.4965 17.9314 12.1218 19 9.4988 19H0.539704C0.248264 19 0 18.7517 0 18.4603Z" />
            </svg>
        </span></div>
    </div>
</a>

<style>
	.talk {
		border-radius: 10px;
		padding: 14px 20px;
		width: 150px;
		box-shadow: 0 0 0 3px rgba(0, 0, 0, 0.7);
		transition: background-color 0.3s;
		overflow: hidden;
		white-space: nowrap;
	}
	.message {
		fill: #47484A;
	}
	.talk:hover {
		background-color:rgba(0, 0, 0, 0.7);
		color: white;
	}
	.talk:hover .ua-description {
		color: white;
		opacity: 1;
	}
	.talk:hover .main-text {
		color: white;
	}
	.talk:hover .message {
		fill: white;
	}
	.top-text {
		display: flex;
		justify-content: space-between;
	}
	.ua-description {
		color:var(--color-text);
		opacity: 0.5;
		font-family: 'MontrealBook';
		-webkit-font-smoothing: antialiased;
	}
	.main-text {
		font-family: 'MontrealMedium';
		font-size: 68px;
		line-height: 68px;
		letter-spacing: -0.02em;
		text-align: left;
		color:var(--color-text);
		-webkit-font-smoothing: antialiased;

	}
	.blink {
		position: absolute;
    	margin-top: -38px;
	}
	a {
		text-decoration: none;
	}

</style>
