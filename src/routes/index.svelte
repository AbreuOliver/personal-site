<script>
	let currentYear = new Date().getFullYear()
	import Footer from "../components/Footer.svelte"
	import ImageLoader from "../components/Image/ImageLoader.svelte";
	// >> Generate random number to stop the images caching
	function rand(min, max) {
		let randomNum = Math.random() * (max - min) + min;
		return Math.round(randomNum);
	}

	import { spring } from 'svelte/motion';

	let coords = spring({ x: 50, y: 50 }, {
		stiffness: 0.1,
		damping: 0.25
	});

	let size = spring(10);
</script>


<svelte:head>
	<title>Oliver Abreu | Front End Developer | Raleigh, NC</title>
</svelte:head>
<!-- <svg
	on:mousemove="{e => coords.set({ x: e.clientX, y: e.clientY })}"
	on:mousedown="{() => size.set(30)}"
	on:mouseup="{() => size.set(10)}"
>
	<circle cx={$coords.x} cy={$coords.y} r={$size}/>
</svg> -->

<!-- HERO SECTION -->
<section class="hero">
	<main>
		<h1 class="hero__heading">Frontend <br/> Developer</h1>
		<p class="hero__paragraph halfWidth">
			I'm a design-oriented web developer who strives to build immersive and beautiful web applications through carefully crafted code and user-centric design. 
		</p>
		<button class="button-33" role="button">Hire Me</button>
	</main>
	<!-- <img class="img" src={`https://i.ibb.co/N90LhRg/macbook-mockup-1.png`} alt="macbook" /> -->
</section>
<!-- ABOUT SECTION -->
<section class="about">
	<h2 class="user-profile__username">
		About <br/> Me
	</h2>
	<!-- <ImageLoader class="user-profile__avatar" src={`https://picsum.photos/seed/${rand(0,200)}/800/800`} alt="Example image"></ImageLoader> -->
	<p>
		Love
	</p>
</section>
<!-- PROJECTS SECTION -->
<section class="projects">
	<h2>
		Selected <br/> Projects
	</h2>
</section>
<section class="contact">
	<h2>
		Reach <br/> Out
	</h2>
</section>
<!-- FOOTER -->
<Footer />


<style>
	/* svg { width: 100%; height: 100%; margin: -8px }
	circle { fill: #ff3e00 } */
	h1 {
		font-size: clamp(2.5rem, 10vw, 4.5rem);
		overflow-wrap: break-word;
		margin: 2rem 0;
		margin-bottom: 3rem;
		line-height: 115%;
		-moz-user-select: none;
		-webkit-user-select: none;
		user-select: none;
		overflow: hidden;
	}
	p {
		font-family: 'Karla', sans-serif;
		font-weight: 400;
		line-height: 175%;
		-moz-user-select: none;
		-webkit-user-select: none;
		user-select: none;
		font-size: 1.5rem;
	}
	section {
		display: grid;
		grid-template-columns:
			1fr
			min(65ch, 90%)
			1fr;
		padding: 3rem 0;
		overflow-x: hidden;
	}
	section > * {
		grid-column: 2;
		width: 100%;
	}

	h2 {
		font-size: clamp(2rem, 8vw, 3.5rem);
		overflow-wrap: break-word;
		margin: 2rem 0;
		margin-bottom: 3rem;
		line-height: 115%;
		-moz-user-select: none;
		-webkit-user-select: none;
		user-select: none;
		overflow: hidden;
	}
	.projects h2, .contact h2 {
		color: #fff;
	}
	/* .img {
		display: block;
		max-height: 15vw;
		width: auto;
		height: auto;
		margin: 0 auto;
		border: 1px solid goldenrod;
		padding: 3rem 0;
	} */

	.halfWidth {
		min-width: 50%;
		max-width: 35ch;
	}

	.about {
		background: #E3E2DF;
	}

	.projects {
		background: #1E1E1E;
		color: #fff;
	}

	.contact {
		background: #102F47;
		color: #fff;
	}

	.hero {
		overflow: hidden;
	}

	main {
		overflow-y: hidden;
	}

	button {
		text-transform: uppercase;
		/* font-family: 'Karla', sans-serif; */
		font-weight: 600;
		font-size: 1.5rem;
	}


</style>