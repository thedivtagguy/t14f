<script>
	import Counter from './Counter.svelte';
	import welcome from '$lib/images/t1.webp';
	import welcome_fallback from '$lib/images/t1.png';
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
		4th Floolr, Sundaram PG
	</h2>

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

	
</style>
