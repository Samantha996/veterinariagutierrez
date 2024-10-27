<script>
	import PawPrint from './PawPrint.svelte';
	import clsx from 'clsx';
	import { gsap } from 'gsap';
	import { onMount } from 'svelte';
	import { ScrollTrigger } from 'gsap/dist/ScrollTrigger';

	onMount(() => {
		gsap.registerPlugin(ScrollTrigger);

		gsap.fromTo(
			'.list__heading',
			{
				y: 100
			},
			{
				y: 0,
				ease: 'power2.inOut',
				duration: 1,
				scrollTrigger: {
					trigger: '.list__heading',
					start: 'top bottom-=10%',
					toggleActions: 'play pause resume reverse'
				}
			}
		);
		gsap.fromTo(
			'.list__headers',
			{
				scale: 0.7,
				opacity: 0.1
			},
			{
				scale: 1,
				opacity: 1,
				ease: 'power2.inOut',
				duration: 1,
				scrollTrigger: {
					trigger: '.list__headers',
					start: 'top bottom-=10%',
					toggleActions: 'play pause resume reverse'
				}
			}
		);
		gsap.fromTo(
			'.list__bullets',
			{
				scale: 0.7,
				opacity: 0.1
			},
			{
				scale: 1,
				opacity: 1,
				ease: 'power2.inOut',
				duration: 1,
				scrollTrigger: {
					trigger: '.list__bullets',
					start: 'top bottom-=20%',
					toggleActions: 'play pause resume reverse'
				}
			}
		);
	});
</script>

<!--bg-gradient-to-b from-gray-100 to-white-->
<section id="servicios" class="background-list">
	<div class="mx-auto max-w-screen-xl px-4 py-8 lg:px-6 lg:py-16">
		<div class="mx-auto mb-8 max-w-screen-md text-center lg:mb-12">
			<h2
				class="list__heading mb-4 bg-clip-text text-center text-4xl
	font-bold not-italic tracking-tight text-gray-900"
			>
				Nuestros Servicios
			</h2>
		</div>
		<div
			class="space-y-8 sm:gap-6 lg:-ml-5 lg:grid lg:grid-cols-2 lg:space-y-0 xl:flex xl:flex-row"
		>
			<!-- Pricing Card -->
			<div
				class="glass-container mx-auto flex max-w-lg flex-col rounded-lg border border-gray-100 p-6 text-center text-gray-900 shadow xl:p-8 dark:border-gray-600 dark:text-gray-900"
			>
				<div class="list__headers relative flex justify-center">
					<h3
						class="absolute inset-0 z-20 flex items-center justify-center text-center text-2xl text-gray-100"
						style="top: 40%;"
					>
						Clinica
					</h3>
					<PawPrint />
				</div>

				<ul role="list" class="list__bullets mb-8 mt-5 space-y-4 text-left text-lg">
					<li class="flex items-center space-x-3">
						<svg
							class="h-5 w-5 flex-shrink-0 text-green-500 dark:text-green-900"
							fill="currentColor"
							viewBox="0 0 20 20"
							xmlns="http://www.w3.org/2000/svg"
							><path
								fill-rule="evenodd"
								d="M16.707 5.293a1 1 0 010 1.414l-8 8a1 1 0 01-1.414 0l-4-4a1 1 0 011.414-1.414L8 12.586l7.293-7.293a1 1 0 011.414 0z"
								clip-rule="evenodd"
							></path></svg
						>
						<span>Vacunacion </span>
					</li>
					<li class="flex items-center space-x-3">
						<svg
							class="h-5 w-5 flex-shrink-0 text-green-500 dark:text-green-900"
							fill="currentColor"
							viewBox="0 0 20 20"
							xmlns="http://www.w3.org/2000/svg"
							><path
								fill-rule="evenodd"
								d="M16.707 5.293a1 1 0 010 1.414l-8 8a1 1 0 01-1.414 0l-4-4a1 1 0 011.414-1.414L8 12.586l7.293-7.293a1 1 0 011.414 0z"
								clip-rule="evenodd"
							></path></svg
						>
						<span> Consultas </span>
					</li>
					<li class="flex items-center space-x-3">
						<svg
							class="h-5 w-5 flex-shrink-0 text-green-500 dark:text-green-900"
							fill="currentColor"
							viewBox="0 0 20 20"
							xmlns="http://www.w3.org/2000/svg"
							><path
								fill-rule="evenodd"
								d="M16.707 5.293a1 1 0 010 1.414l-8 8a1 1 0 01-1.414 0l-4-4a1 1 0 011.414-1.414L8 12.586l7.293-7.293a1 1 0 011.414 0z"
								clip-rule="evenodd"
							></path></svg
						>
						<span>Hospitalizaciones</span>
					</li>
				</ul>
			</div>
			<div
				class="glass-container mx-auto flex max-w-lg flex-col rounded-lg border border-gray-100 bg-white p-6 text-center text-gray-900 shadow xl:p-8 dark:border-gray-600 dark:bg-blue-300 dark:text-gray-900"
			>
				<div class="list__headers relative flex justify-center">
					<h3
						class="absolute inset-0 z-20 flex items-center justify-center text-center text-2xl text-gray-100"
						style="top: 40%;"
					>
						Laboratorio
					</h3>
					<PawPrint />
				</div>

				<!-- List -->
				<ul role="list" class="list__bullets mb-8 mt-5 space-y-4 text-left text-lg">
					<li class="flex items-center space-x-3">
						<!-- Icon -->
						<svg
							class="h-5 w-5 flex-shrink-0 text-green-500 dark:text-green-900"
							fill="currentColor"
							viewBox="0 0 20 20"
							xmlns="http://www.w3.org/2000/svg"
							><path
								fill-rule="evenodd"
								d="M16.707 5.293a1 1 0 010 1.414l-8 8a1 1 0 01-1.414 0l-4-4a1 1 0 011.414-1.414L8 12.586l7.293-7.293a1 1 0 011.414 0z"
								clip-rule="evenodd"
							></path></svg
						>
						<span> Hemogramas </span>
					</li>
					<li class="flex items-center space-x-3">
						<!-- Icon -->
						<svg
							class="h-5 w-5 flex-shrink-0 text-green-500 dark:text-green-900"
							fill="currentColor"
							viewBox="0 0 20 20"
							xmlns="http://www.w3.org/2000/svg"
							><path
								fill-rule="evenodd"
								d="M16.707 5.293a1 1 0 010 1.414l-8 8a1 1 0 01-1.414 0l-4-4a1 1 0 011.414-1.414L8 12.586l7.293-7.293a1 1 0 011.414 0z"
								clip-rule="evenodd"
							></path></svg
						>
						<span> Quimica Sanguinea </span>
					</li>
					<li class="flex items-center space-x-3">
						<!-- Icon -->
						<svg
							class="h-5 w-5 flex-shrink-0 text-green-500 dark:text-green-900"
							fill="currentColor"
							viewBox="0 0 20 20"
							xmlns="http://www.w3.org/2000/svg"
							><path
								fill-rule="evenodd"
								d="M16.707 5.293a1 1 0 010 1.414l-8 8a1 1 0 01-1.414 0l-4-4a1 1 0 011.414-1.414L8 12.586l7.293-7.293a1 1 0 011.414 0z"
								clip-rule="evenodd"
							></path></svg
						>
						<span> Generales de Orina </span>
					</li>
					<li class="flex items-center space-x-3">
						<!-- Icon -->
						<svg
							class="h-5 w-5 flex-shrink-0 text-green-500 dark:text-green-900"
							fill="currentColor"
							viewBox="0 0 20 20"
							xmlns="http://www.w3.org/2000/svg"
							><path
								fill-rule="evenodd"
								d="M16.707 5.293a1 1 0 010 1.414l-8 8a1 1 0 01-1.414 0l-4-4a1 1 0 011.414-1.414L8 12.586l7.293-7.293a1 1 0 011.414 0z"
								clip-rule="evenodd"
							></path></svg
						>
						<span>Rayos X </span>
					</li>
					<li class="flex items-center space-x-3">
						<!-- Icon -->
						<svg
							class="h-5 w-5 flex-shrink-0 text-green-500 dark:text-green-900"
							fill="currentColor"
							viewBox="0 0 20 20"
							xmlns="http://www.w3.org/2000/svg"
							><path
								fill-rule="evenodd"
								d="M16.707 5.293a1 1 0 010 1.414l-8 8a1 1 0 01-1.414 0l-4-4a1 1 0 011.414-1.414L8 12.586l7.293-7.293a1 1 0 011.414 0z"
								clip-rule="evenodd"
							></path></svg
						>
						<span> Ultrasonidos </span>
					</li>
					<li class="flex items-center space-x-3">
						<!-- Icon -->
						<svg
							class="h-5 w-5 flex-shrink-0 text-green-500 dark:text-green-900"
							fill="currentColor"
							viewBox="0 0 20 20"
							xmlns="http://www.w3.org/2000/svg"
							><path
								fill-rule="evenodd"
								d="M16.707 5.293a1 1 0 010 1.414l-8 8a1 1 0 01-1.414 0l-4-4a1 1 0 011.414-1.414L8 12.586l7.293-7.293a1 1 0 011.414 0z"
								clip-rule="evenodd"
							></path></svg
						>
						<span>Niveles de Progesteronas</span>
					</li>
				</ul>
			</div>
			<div
				class="glass-container mx-auto flex max-w-lg flex-col rounded-lg border border-gray-100 bg-white p-6 text-center text-gray-900 shadow xl:p-8 dark:border-gray-600 dark:bg-blue-300 dark:text-gray-900"
			>
				<div class="list__headers relative flex justify-center">
					<h3
						class="absolute inset-0 z-20 flex items-center justify-center text-center text-2xl text-gray-100"
						style="top: 40%;"
					>
						Cirugia
					</h3>
					<PawPrint />
				</div>
				<!-- List -->
				<ul role="list" class="list__bullets mb-8 mt-5 space-y-4 text-left text-lg">
					<li class="flex items-center space-x-3">
						<!-- Icon -->
						<svg
							class="h-5 w-5 flex-shrink-0 text-green-500 dark:text-green-900"
							fill="currentColor"
							viewBox="0 0 20 20"
							xmlns="http://www.w3.org/2000/svg"
							><path
								fill-rule="evenodd"
								d="M16.707 5.293a1 1 0 010 1.414l-8 8a1 1 0 01-1.414 0l-4-4a1 1 0 011.414-1.414L8 12.586l7.293-7.293a1 1 0 011.414 0z"
								clip-rule="evenodd"
							></path></svg
						>
						<span>Esterlizacion </span>
					</li>
					<li class="flex items-center space-x-3">
						<!-- Icon -->
						<svg
							class="h-5 w-5 flex-shrink-0 text-green-500 dark:text-green-900"
							fill="currentColor"
							viewBox="0 0 20 20"
							xmlns="http://www.w3.org/2000/svg"
							><path
								fill-rule="evenodd"
								d="M16.707 5.293a1 1 0 010 1.414l-8 8a1 1 0 01-1.414 0l-4-4a1 1 0 011.414-1.414L8 12.586l7.293-7.293a1 1 0 011.414 0z"
								clip-rule="evenodd"
							></path></svg
						>
						<span> Cesarea </span>
					</li>
					<li class="flex items-center space-x-3">
						<!-- Icon -->
						<svg
							class="h-5 w-5 flex-shrink-0 text-green-500 dark:text-green-900"
							fill="currentColor"
							viewBox="0 0 20 20"
							xmlns="http://www.w3.org/2000/svg"
							><path
								fill-rule="evenodd"
								d="M16.707 5.293a1 1 0 010 1.414l-8 8a1 1 0 01-1.414 0l-4-4a1 1 0 011.414-1.414L8 12.586l7.293-7.293a1 1 0 011.414 0z"
								clip-rule="evenodd"
							></path></svg
						>
						<span> Ortopedia </span>
					</li>
					<li class="flex items-center space-x-3">
						<!-- Icon -->
						<svg
							class="h-5 w-5 flex-shrink-0 text-green-500 dark:text-green-900"
							fill="currentColor"
							viewBox="0 0 20 20"
							xmlns="http://www.w3.org/2000/svg"
							><path
								fill-rule="evenodd"
								d="M16.707 5.293a1 1 0 010 1.414l-8 8a1 1 0 01-1.414 0l-4-4a1 1 0 011.414-1.414L8 12.586l7.293-7.293a1 1 0 011.414 0z"
								clip-rule="evenodd"
							></path></svg
						>
						<span> Profilaxis Dental </span>
					</li>
					<li class="flex items-center space-x-3">
						<!-- Icon -->
						<svg
							class="h-5 w-5 flex-shrink-0 text-green-500 dark:text-green-900"
							fill="currentColor"
							viewBox="0 0 20 20"
							xmlns="http://www.w3.org/2000/svg"
							><path
								fill-rule="evenodd"
								d="M16.707 5.293a1 1 0 010 1.414l-8 8a1 1 0 01-1.414 0l-4-4a1 1 0 011.414-1.414L8 12.586l7.293-7.293a1 1 0 011.414 0z"
								clip-rule="evenodd"
							></path></svg
						>
						<span> Laparatomia </span>
					</li>
					<li class="flex items-center space-x-3">
						<!-- Icon -->
						<svg
							class="h-5 w-5 flex-shrink-0 text-green-500 dark:text-green-900"
							fill="currentColor"
							viewBox="0 0 20 20"
							xmlns="http://www.w3.org/2000/svg"
							><path
								fill-rule="evenodd"
								d="M16.707 5.293a1 1 0 010 1.414l-8 8a1 1 0 01-1.414 0l-4-4a1 1 0 011.414-1.414L8 12.586l7.293-7.293a1 1 0 011.414 0z"
								clip-rule="evenodd"
							></path></svg
						>
						<span> Cistotomia </span>
					</li>
					<li class="flex items-center space-x-3">
						<!-- Icon -->
						<svg
							class="h-5 w-5 flex-shrink-0 text-green-500 dark:text-green-900"
							fill="currentColor"
							viewBox="0 0 20 20"
							xmlns="http://www.w3.org/2000/svg"
							><path
								fill-rule="evenodd"
								d="M16.707 5.293a1 1 0 010 1.414l-8 8a1 1 0 01-1.414 0l-4-4a1 1 0 011.414-1.414L8 12.586l7.293-7.293a1 1 0 011.414 0z"
								clip-rule="evenodd"
							></path></svg
						>
						<span> Excicion Tumoral </span>
					</li>
					<li class="flex items-center space-x-3">
						<!-- Icon -->
						<svg
							class="h-5 w-5 flex-shrink-0 text-green-500 dark:text-green-900"
							fill="currentColor"
							viewBox="0 0 20 20"
							xmlns="http://www.w3.org/2000/svg"
							><path
								fill-rule="evenodd"
								d="M16.707 5.293a1 1 0 010 1.414l-8 8a1 1 0 01-1.414 0l-4-4a1 1 0 011.414-1.414L8 12.586l7.293-7.293a1 1 0 011.414 0z"
								clip-rule="evenodd"
							></path></svg
						>
						<span> Esplenctomimia </span>
					</li>
					<li class="flex items-center space-x-3">
						<!-- Icon -->
						<svg
							class="h-5 w-5 flex-shrink-0 text-green-500 dark:text-green-900"
							fill="currentColor"
							viewBox="0 0 20 20"
							xmlns="http://www.w3.org/2000/svg"
							><path
								fill-rule="evenodd"
								d="M16.707 5.293a1 1 0 010 1.414l-8 8a1 1 0 01-1.414 0l-4-4a1 1 0 011.414-1.414L8 12.586l7.293-7.293a1 1 0 011.414 0z"
								clip-rule="evenodd"
							></path></svg
						>
						<span> Enuclacion Ocular </span>
					</li>
					<li class="flex items-center space-x-3">
						<!-- Icon -->
						<svg
							class="h-5 w-5 flex-shrink-0 text-green-500 dark:text-green-900"
							fill="currentColor"
							viewBox="0 0 20 20"
							xmlns="http://www.w3.org/2000/svg"
							><path
								fill-rule="evenodd"
								d="M16.707 5.293a1 1 0 010 1.414l-8 8a1 1 0 01-1.414 0l-4-4a1 1 0 011.414-1.414L8 12.586l7.293-7.293a1 1 0 011.414 0z"
								clip-rule="evenodd"
							></path></svg
						>
						<span> Limpieza de Oidos Profunda </span>
					</li>
				</ul>
			</div>
			<div
				class="glass-container mx-auto flex max-w-lg flex-col rounded-lg border border-gray-100 bg-white p-6 text-center text-gray-900 shadow xl:p-8 dark:border-gray-600 dark:bg-blue-300 dark:text-gray-900"
			>
				<div class="list__headers relative flex justify-center">
					<h3
						class="absolute inset-0 z-20 flex items-center justify-center text-center text-2xl text-gray-100"
						style="top: 40%;"
					>
						Estetica
					</h3>
					<PawPrint />
				</div>

				<!-- List -->
				<ul role="list" class="list__bullets mb-8 mt-5 space-y-4 text-left text-lg">
					<li class="flex items-center space-x-3">
						<!-- Icon -->
						<svg
							class="h-5 w-5 flex-shrink-0 text-green-500 dark:text-green-900"
							fill="currentColor"
							viewBox="0 0 20 20"
							xmlns="http://www.w3.org/2000/svg"
							><path
								fill-rule="evenodd"
								d="M16.707 5.293a1 1 0 010 1.414l-8 8a1 1 0 01-1.414 0l-4-4a1 1 0 011.414-1.414L8 12.586l7.293-7.293a1 1 0 011.414 0z"
								clip-rule="evenodd"
							></path></svg
						>
						<span> Corte de Pelo </span>
					</li>
					<li class="flex items-center space-x-3">
						<!-- Icon -->
						<svg
							class="h-5 w-5 flex-shrink-0 text-green-500 dark:text-green-900"
							fill="currentColor"
							viewBox="0 0 20 20"
							xmlns="http://www.w3.org/2000/svg"
							><path
								fill-rule="evenodd"
								d="M16.707 5.293a1 1 0 010 1.414l-8 8a1 1 0 01-1.414 0l-4-4a1 1 0 011.414-1.414L8 12.586l7.293-7.293a1 1 0 011.414 0z"
								clip-rule="evenodd"
							></path></svg
						>
						<span>Baño </span>
					</li>
					<li class="flex items-center space-x-3">
						<!-- Icon -->
						<svg
							class="h-5 w-5 flex-shrink-0 text-green-500 dark:text-green-900"
							fill="currentColor"
							viewBox="0 0 20 20"
							xmlns="http://www.w3.org/2000/svg"
							><path
								fill-rule="evenodd"
								d="M16.707 5.293a1 1 0 010 1.414l-8 8a1 1 0 01-1.414 0l-4-4a1 1 0 011.414-1.414L8 12.586l7.293-7.293a1 1 0 011.414 0z"
								clip-rule="evenodd"
							></path></svg
						>
						<span> Baño Medicado </span>
					</li>
					<li class="flex items-center space-x-3">
						<!-- Icon -->
						<svg
							class="h-5 w-5 flex-shrink-0 text-green-500 dark:text-green-900"
							fill="currentColor"
							viewBox="0 0 20 20"
							xmlns="http://www.w3.org/2000/svg"
							><path
								fill-rule="evenodd"
								d="M16.707 5.293a1 1 0 010 1.414l-8 8a1 1 0 01-1.414 0l-4-4a1 1 0 011.414-1.414L8 12.586l7.293-7.293a1 1 0 011.414 0z"
								clip-rule="evenodd"
							></path></svg
						>
						<span> Corte de Uñas </span>
					</li>
					<li class="flex items-center space-x-3">
						<!-- Icon -->
						<svg
							class="h-5 w-5 flex-shrink-0 text-green-500 dark:text-green-900"
							fill="currentColor"
							viewBox="0 0 20 20"
							xmlns="http://www.w3.org/2000/svg"
							><path
								fill-rule="evenodd"
								d="M16.707 5.293a1 1 0 010 1.414l-8 8a1 1 0 01-1.414 0l-4-4a1 1 0 011.414-1.414L8 12.586l7.293-7.293a1 1 0 011.414 0z"
								clip-rule="evenodd"
							></path></svg
						>
						<span>Limpieza de Oidos</span>
					</li>
				</ul>
			</div>
		</div>
	</div>
</section>

<style>
	.background-list {
		background-image: url('/list_background.svg');
	}
	.glass-container {
		background: rgba(255, 255, 255, 0.2);
		border-radius: 16px;
		box-shadow: 0 4px 30px rgba(0, 0, 0, 0.1);
		backdrop-filter: blur(5px);
		-webkit-backdrop-filter: blur(5px);
		border: 1px solid rgba(255, 255, 255, 0.3);
	}
</style>
