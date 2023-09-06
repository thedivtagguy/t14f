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

	<picture>
		<img class="framed flat" src={flat} alt="My room" />
		<caption class="caption">The greatest, most prosperous sovereign entity in Yelahanka, Bangalore <br/> since Sri Devi Grand</caption>
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
		margin: 2rem 0;
	}

	h2 {
		font-size: 1.5rem;
		text-transform: uppercase;
		font-weight: 600;
		letter-spacing: 0.7rem;
	}

	span.welcome-text {
		font-weight: 300;
		font-style: italic;
	}

	span.italics {
		font-style: italic;
		font-weight: 300;
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
	}

	.flat {
		margin-top: 100rem;
		max-width: 500px;
		padding: 10px;
	}
</style>
