<script>
	import Counter from './Counter.svelte';
	import welcome from '$lib/images/t1.webp';
	import welcome_fallback from '$lib/images/t1.png';
	import flat from '$lib/images/room.jpg';
	import willBeBack from '$lib/images/willbeback.jpg'
</script>

<svelte:head>
	<title>T14F | Home</title>
	<meta name="description" content="T1, 4th Floolr" />
</svelte:head>

<section>
	<h1>
		<span class="welcome-text">Welcome to</span><br />the Offices <span class="italics">of</span>
		<span class="welcome">
			<picture>
				<source srcset={welcome} type="image/webp" />
				<img src={welcome_fallback} alt="Welcome" />
			</picture>
		</span>

		
	</h1>

	<h2>
		<a href="https://4thfloolr.com">4th Floolr</a>, Sundaram PG
	</h2>
	<iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d840.8458084785633!2d77.56760026697779!3d13.105916565637383!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x3bae199fa7e3828f%3A0x15885e21ec389825!2sT1%20Sundarbois!5e0!3m2!1sen!2sin!4v1694014984657!5m2!1sen!2sin"  height="600" style="border:0;" allowfullscreen="" loading="lazy" referrerpolicy="no-referrer-when-downgrade"></iframe>
	<caption>A fine, well-reviewed establishment nestled within an eccentric locale</caption>
	<picture>
		<img class="framed flat" src={flat} alt="My room" />
		<caption class="caption">The greatest, most prosperous sovereign entity in Yelahanka, Bangalore <br class="sri"/> since Sri Devi Grand</caption>
	</picture>

	<picture>
		<img class="framed flat" src={willBeBack} alt="My room" />
		<caption class="caption">We'll be back shortly.</caption>
	</picture>

</section>

<style>
	section {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		flex: 0.6;
	}

	h1 {
		width: 100%;
		font-size: 5rem;
		line-height: 1.1;
		margin: 12rem 0 3rem 0;
	}

	h2 {
		font-size: 1.5rem;
		text-transform: uppercase;
		font-weight: 600;
		letter-spacing: 0.7rem;
		line-height: 1.8;
	}

	iframe {
		margin-top: 100rem;
		width: 100%;
		max-width: 900px;
	}

	span.welcome-text {
		font-weight: 300;
		font-style: italic;
	}

	span.italics {
		font-style: italic;
		font-weight: 300;
	}
caption{
	padding-top: 0.5rem;
}
	.welcome {
		display: block;
		position: relative;
		width: 50%;
		height: 100%;
		padding: 0 0 calc(100% * 495 / 2048) 0;
		margin: auto;
	}

	.welcome img {
		position: absolute;
		width: 100%;
		height: 100%;
		top: 0;
		padding: 0.8rem 0;
		display: block;
		filter: drop-shadow(5px 15px 10px #222222c1)
	}

	/* Media query for screens smaller than 768px (typical mobile screens) */
	@media screen and (max-width: 768px) {
		h1 {
			font-size: 3rem; /* Decrease the font size for better mobile readability */
			margin: 12rem 0 2rem 0;

		}

		h2 {
			font-size: 1.2rem; /* Decrease the font size for better mobile readability */
			letter-spacing: 0.3rem;
			width: 60%;
			text-align: center;
		}

		.welcome {
			width: 50%; /* Adjust the image width for smaller screens */
		}

		.flat {
		margin-top: 100rem;
		max-width: 500px;
	}
	}

	.flat {
		margin-top: 100rem;
		max-width: 800px;
	}
</style>
