<script>
	import { onMount } from 'svelte';
	import { gsap } from 'gsap'; // Make sure you have GSAP installed

	let ball;
	const colors = ['#480e6e', '#fc4239', '#ffd400', '#00c4df'];

	function play() {
		const screenWidth = window.innerWidth;
		const horizontalDistance = screenWidth <= 640 ? 350 : 450; // 300px for mobile, 450px for larger screens

		// Setting the initial position of the ball
		gsap.set(ball, { y: 100, x: -250 });

		// Creating a timeline
		let tl = gsap.timeline({ delay: 0.5 });

		// Animating the ball
		tl.to(ball, { duration: 0.5, y: 0 }) // Move up
			.to(ball, { duration: 1.25, y: 150, ease: 'bounce.out' }) // Drop down with bounce effect
			.to(ball, { duration: 2.5, x: `+=${horizontalDistance}` }, '-=2') // Move horizontally
			.to(ball, { duration: 2, x: -250, y: 100, backgroundColor: gsap.utils.random(colors) }, '+=1') // Return and change color
			.call(play); // Recursively call the play function to loop
	}
	onMount(() => {
		play(); // Start the animation when the component is mounted
	});
</script>

<div id="ball" bind:this={ball}></div>

<style>
	#ball {
		width: 100px;
		height: 100px;
		border-radius: 50%;
		background-color: #480e6e;
		position: relative;
	}
</style>
