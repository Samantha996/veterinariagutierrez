<script>
	import { onMount } from 'svelte';
	import Ball from './Ball.svelte';
	import Logo from './Logo.svelte';
	import MainLogo from './MainLogo.svelte';
	import { gsap } from 'gsap'; // Make sure you have GSAP installed
	import Ratings from './Ratings.svelte';

	onMount(() => {
		const tl = gsap.timeline({ defaults: { ease: 'power2.inOut' } });

		tl.fromTo('.hero__heading', { scale: 0.5 }, { scale: 1, opacity: 1, duration: 1.4 });
		tl.fromTo('.hero__body', { y: 200 }, { y: 0, opacity: 1, duration: 1.2 }, '-=0.6');
		tl.fromTo(
			'.hero__image',
			{ y: 0, scale: 0.4, opacity: 0 },
			{ y: 0, opacity: 1, duration: 1.3, scale: 1 },
			'+=0.3'
		);
		tl.fromTo('.hero__glow', { scale: 0.5 }, { scale: 1, opacity: 1, duration: 1.8 }, '-=1');
	});
</script>

<div
	class="background-main relative mx-0 -mb-72 -mt-48 flex flex-col-reverse lg:flex-row"
	id="home"
>
	<!-- Image Section -->
	<div class="-z-20 order-1 my-10 lg:order-1">
		<!-- svelte-ignore a11y-img-redundant-alt -->
		<img
			src="images/VG.png"
			alt="Background Image"
			class="hero__image opacity-1 -mt-96 h-[140vh] w-full object-cover lg:mt-0"
			style="object-position: top;"
		/>
	</div>

	<div class="relative order-2 mt-10 px-5 lg:order-2 lg:mr-48 lg:px-0">
		<div class="absolute inset-0 -z-10 mt-40 flex justify-center">
			<Ball />
		</div>

		<div>
			<div class="hero__heading flex justify-center">
				<MainLogo />
			</div>
		</div>

		<!-- Heading -->
		<h3
			class="hero__body -mt-40 bg-gradient-to-b from-blue-100
			to-blue-900 bg-clip-text text-center text-2xl not-italic text-transparent"
		>
			Treinta años de experiencia cuidando a tu mejor amigo.
		</h3>

		<!-- Paragraph -->
		<p class="hero__body mt-5 justify-center text-center text-lg lg:max-w-[600px]">
			Nuestra misión es ofrecerle a usted y su mascota el mejor servicio de cuidado y atención. En
			nuestras instalaciones contamos con servicios médicos como vacunación, consulta general,
			cirugía general, ortopedia, salud dental, y de estética canina y felina.
		</p>
		<div class="ratings mobile:mb-10 mt-0 flex items-center justify-center lg:mt-5">
			<a href="https://g.co/kgs/SA2Bcrt">
				<Ratings />
			</a>
		</div>
	</div>
</div>

<style>
	@media only screen and (max-width: 600px) {
		.hero__body {
			margin-bottom: 40px;
		}
		.ratings {
			margin-top: -10px;
		}
	}
	.background-main {
		background-image: url('/main_background.svg');
	}
	@media (max-width: 1024px) {
		.background-main {
			background-size: 150%; /* Zoom in slightly on tablet screens */
			background-position: top; /* Adjust the position for tablet */
		}
	}
	/* Media query for mobile screens */
	@media (max-width: 768px) {
		.background-main {
			background-size: 200%; /* Zoom in to show fewer circles on smaller screens */
			background-position: top; /* Position to control which part of the SVG is shown */
		}
	}
</style>
