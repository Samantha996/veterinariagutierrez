<script>
	import { onMount } from 'svelte';
	import PawPrint from './PawPrint.svelte';

	// Function to set equal height for all boxes
	onMount(() => {
		const boxes = document.querySelectorAll('.box');
		let maxHeight = 0;

		// Find the maximum height
		boxes.forEach((box) => {
			const height = box.offsetHeight;
			if (height > maxHeight) {
				maxHeight = height;
			}
		});

		// Set all boxes to the maximum height
		boxes.forEach((box) => {
			box.style.height = `${maxHeight}px`;
		});
	});
</script>

<h2 class=" p-5 text-center text-4xl">Nuestros Servicios</h2>

<!-- Flexbox container for PawPrints and Titles -->
<div class="block items-start justify-center gap-x-28 md:flex md:flex-row">
	<div class="flex flex-col items-center">
		<div class="relative flex justify-center">
			<h3
				class="absolute inset-0 z-20 flex items-center justify-center text-center text-2xl text-gray-100"
				style="top: 40%;"
			>
				Clinica
			</h3>
			<PawPrint />
		</div>
		<div
			class="box mb-5 mt-4 w-72 flex-grow rounded-lg border-4 border-blue-900 bg-gray-800 p-5 text-gray-200"
		>
			<ul role="list" class="mb-8 space-y-4 text-left">
				<li class="flex items-center space-x-3">
					<!-- Icon -->
					<svg
						class="h-5 w-5 flex-shrink-0 text-green-500 dark:text-green-400"
						fill="currentColor"
						viewBox="0 0 20 20"
						xmlns="http://www.w3.org/2000/svg"
						><path
							fill-rule="evenodd"
							d="M16.707 5.293a1 1 0 010 1.414l-8 8a1 1 0 01-1.414 0l-4-4a1 1 0 011.414-1.414L8 12.586l7.293-7.293a1 1 0 011.414 0z"
							clip-rule="evenodd"
						></path></svg
					>
					<span class="font-semibold">Vacunacion</span>
				</li>
				<li class="flex items-center space-x-3">
					<!-- Icon -->
					<svg
						class="h-5 w-5 flex-shrink-0 text-green-500 dark:text-green-400"
						fill="currentColor"
						viewBox="0 0 20 20"
						xmlns="http://www.w3.org/2000/svg"
						><path
							fill-rule="evenodd"
							d="M16.707 5.293a1 1 0 010 1.414l-8 8a1 1 0 01-1.414 0l-4-4a1 1 0 011.414-1.414L8 12.586l7.293-7.293a1 1 0 011.414 0z"
							clip-rule="evenodd"
						></path></svg
					>
					<span class="font-semibold">Consultas</span>
				</li>
				<li class="flex items-center space-x-3">
					<!-- Icon -->
					<svg
						class="h-5 w-5 flex-shrink-0 text-green-500 dark:text-green-400"
						fill="currentColor"
						viewBox="0 0 20 20"
						xmlns="http://www.w3.org/2000/svg"
						><path
							fill-rule="evenodd"
							d="M16.707 5.293a1 1 0 010 1.414l-8 8a1 1 0 01-1.414 0l-4-4a1 1 0 011.414-1.414L8 12.586l7.293-7.293a1 1 0 011.414 0z"
							clip-rule="evenodd"
						></path></svg
					>
					<span class="font-semibold">Hospitalizaciones</span>
				</li>
			</ul>
		</div>
	</div>

	<div class="flex flex-col items-center">
		<div class="relative flex justify-center">
			<h3
				class="absolute inset-0 z-20 flex items-center justify-center text-center text-2xl text-gray-100"
				style="top: 40%;"
			>
				Laboratorio
			</h3>
			<PawPrint />
		</div>
		<div
			class="box mb-5 mt-4 w-72 flex-grow rounded-lg border-4 border-blue-900 bg-gray-800 p-5 text-gray-200"
		>
			<ul role="list" class="mb-8 space-y-4 text-left">
				<li class="flex items-center space-x-3">
					<!-- Icon -->
					<svg
						class="h-5 w-5 flex-shrink-0 text-green-500 dark:text-green-400"
						fill="currentColor"
						viewBox="0 0 20 20"
						xmlns="http://www.w3.org/2000/svg"
						><path
							fill-rule="evenodd"
							d="M16.707 5.293a1 1 0 010 1.414l-8 8a1 1 0 01-1.414 0l-4-4a1 1 0 011.414-1.414L8 12.586l7.293-7.293a1 1 0 011.414 0z"
							clip-rule="evenodd"
						></path></svg
					>
					<span class="font-semibold">Hemogramas</span>
				</li>
				<li class="flex items-center space-x-3">
					<!-- Icon -->
					<svg
						class="h-5 w-5 flex-shrink-0 text-green-500 dark:text-green-400"
						fill="currentColor"
						viewBox="0 0 20 20"
						xmlns="http://www.w3.org/2000/svg"
						><path
							fill-rule="evenodd"
							d="M16.707 5.293a1 1 0 010 1.414l-8 8a1 1 0 01-1.414 0l-4-4a1 1 0 011.414-1.414L8 12.586l7.293-7.293a1 1 0 011.414 0z"
							clip-rule="evenodd"
						></path></svg
					>
					<span class="font-semibold">Quimica Sanguinea</span>
				</li>
				<li class="flex items-center space-x-3">
					<!-- Icon -->
					<svg
						class="h-5 w-5 flex-shrink-0 text-green-500 dark:text-green-400"
						fill="currentColor"
						viewBox="0 0 20 20"
						xmlns="http://www.w3.org/2000/svg"
						><path
							fill-rule="evenodd"
							d="M16.707 5.293a1 1 0 010 1.414l-8 8a1 1 0 01-1.414 0l-4-4a1 1 0 011.414-1.414L8 12.586l7.293-7.293a1 1 0 011.414 0z"
							clip-rule="evenodd"
						></path></svg
					>
					<span class="font-semibold">Generales de Orina</span>
				</li>
				<li class="flex items-center space-x-3">
					<!-- Icon -->
					<svg
						class="h-5 w-5 flex-shrink-0 text-green-500 dark:text-green-400"
						fill="currentColor"
						viewBox="0 0 20 20"
						xmlns="http://www.w3.org/2000/svg"
						><path
							fill-rule="evenodd"
							d="M16.707 5.293a1 1 0 010 1.414l-8 8a1 1 0 01-1.414 0l-4-4a1 1 0 011.414-1.414L8 12.586l7.293-7.293a1 1 0 011.414 0z"
							clip-rule="evenodd"
						></path></svg
					>
					<span class="font-semibold">Rayos X</span>
				</li>
				<li class="flex items-center space-x-3">
					<!-- Icon -->
					<svg
						class="h-5 w-5 flex-shrink-0 text-green-500 dark:text-green-400"
						fill="currentColor"
						viewBox="0 0 20 20"
						xmlns="http://www.w3.org/2000/svg"
						><path
							fill-rule="evenodd"
							d="M16.707 5.293a1 1 0 010 1.414l-8 8a1 1 0 01-1.414 0l-4-4a1 1 0 011.414-1.414L8 12.586l7.293-7.293a1 1 0 011.414 0z"
							clip-rule="evenodd"
						></path></svg
					>
					<span class="font-semibold">Ultrasonidos</span>
				</li>
				<li class="flex items-center space-x-3">
					<!-- Icon -->
					<svg
						class="h-5 w-5 flex-shrink-0 text-green-500 dark:text-green-400"
						fill="currentColor"
						viewBox="0 0 20 20"
						xmlns="http://www.w3.org/2000/svg"
						><path
							fill-rule="evenodd"
							d="M16.707 5.293a1 1 0 010 1.414l-8 8a1 1 0 01-1.414 0l-4-4a1 1 0 011.414-1.414L8 12.586l7.293-7.293a1 1 0 011.414 0z"
							clip-rule="evenodd"
						></path></svg
					>
					<span class="font-semibold">Niveles de Progesteronas</span>
				</li>
			</ul>
		</div>
	</div>

	<div class="flex flex-col items-center">
		<div class="relative flex justify-center">
			<h3
				class="absolute inset-0 z-20 flex items-center justify-center text-center text-2xl text-gray-100"
				style="top: 40%;"
			>
				Cirugia
			</h3>
			<PawPrint />
		</div>
		<div
			class="box mb-5 mt-4 w-72 flex-grow rounded-lg border-4 border-blue-900 bg-gray-800 p-5 text-gray-200"
		>
			<ul role="list" class="mb-8 space-y-4 text-left">
				<li class="flex items-center space-x-3">
					<!-- Icon -->
					<svg
						class="h-5 w-5 flex-shrink-0 text-green-500 dark:text-green-400"
						fill="currentColor"
						viewBox="0 0 20 20"
						xmlns="http://www.w3.org/2000/svg"
						><path
							fill-rule="evenodd"
							d="M16.707 5.293a1 1 0 010 1.414l-8 8a1 1 0 01-1.414 0l-4-4a1 1 0 011.414-1.414L8 12.586l7.293-7.293a1 1 0 011.414 0z"
							clip-rule="evenodd"
						></path></svg
					>
					<span class="font-semibold">Esterlizacion</span>
				</li>
				<li class="flex items-center space-x-3">
					<!-- Icon -->
					<svg
						class="h-5 w-5 flex-shrink-0 text-green-500 dark:text-green-400"
						fill="currentColor"
						viewBox="0 0 20 20"
						xmlns="http://www.w3.org/2000/svg"
						><path
							fill-rule="evenodd"
							d="M16.707 5.293a1 1 0 010 1.414l-8 8a1 1 0 01-1.414 0l-4-4a1 1 0 011.414-1.414L8 12.586l7.293-7.293a1 1 0 011.414 0z"
							clip-rule="evenodd"
						></path></svg
					>
					<span class="font-semibold">Cesarea</span>
				</li>
				<li class="flex items-center space-x-3">
					<!-- Icon -->
					<svg
						class="h-5 w-5 flex-shrink-0 text-green-500 dark:text-green-400"
						fill="currentColor"
						viewBox="0 0 20 20"
						xmlns="http://www.w3.org/2000/svg"
						><path
							fill-rule="evenodd"
							d="M16.707 5.293a1 1 0 010 1.414l-8 8a1 1 0 01-1.414 0l-4-4a1 1 0 011.414-1.414L8 12.586l7.293-7.293a1 1 0 011.414 0z"
							clip-rule="evenodd"
						></path></svg
					>
					<span class="font-semibold">Ortopedia</span>
				</li>
				<li class="flex items-center space-x-3">
					<!-- Icon -->
					<svg
						class="h-5 w-5 flex-shrink-0 text-green-500 dark:text-green-400"
						fill="currentColor"
						viewBox="0 0 20 20"
						xmlns="http://www.w3.org/2000/svg"
						><path
							fill-rule="evenodd"
							d="M16.707 5.293a1 1 0 010 1.414l-8 8a1 1 0 01-1.414 0l-4-4a1 1 0 011.414-1.414L8 12.586l7.293-7.293a1 1 0 011.414 0z"
							clip-rule="evenodd"
						></path></svg
					>
					<span class="font-semibold">Profilaxis Dental</span>
				</li>
				<li class="flex items-center space-x-3">
					<!-- Icon -->
					<svg
						class="h-5 w-5 flex-shrink-0 text-green-500 dark:text-green-400"
						fill="currentColor"
						viewBox="0 0 20 20"
						xmlns="http://www.w3.org/2000/svg"
						><path
							fill-rule="evenodd"
							d="M16.707 5.293a1 1 0 010 1.414l-8 8a1 1 0 01-1.414 0l-4-4a1 1 0 011.414-1.414L8 12.586l7.293-7.293a1 1 0 011.414 0z"
							clip-rule="evenodd"
						></path></svg
					>
					<span class="font-semibold">Laparatomia</span>
				</li>
				<li class="flex items-center space-x-3">
					<!-- Icon -->
					<svg
						class="h-5 w-5 flex-shrink-0 text-green-500 dark:text-green-400"
						fill="currentColor"
						viewBox="0 0 20 20"
						xmlns="http://www.w3.org/2000/svg"
						><path
							fill-rule="evenodd"
							d="M16.707 5.293a1 1 0 010 1.414l-8 8a1 1 0 01-1.414 0l-4-4a1 1 0 011.414-1.414L8 12.586l7.293-7.293a1 1 0 011.414 0z"
							clip-rule="evenodd"
						></path></svg
					>
					<span class="font-semibold">Cistotomia</span>
				</li>
				<li class="flex items-center space-x-3">
					<!-- Icon -->
					<svg
						class="h-5 w-5 flex-shrink-0 text-green-500 dark:text-green-400"
						fill="currentColor"
						viewBox="0 0 20 20"
						xmlns="http://www.w3.org/2000/svg"
						><path
							fill-rule="evenodd"
							d="M16.707 5.293a1 1 0 010 1.414l-8 8a1 1 0 01-1.414 0l-4-4a1 1 0 011.414-1.414L8 12.586l7.293-7.293a1 1 0 011.414 0z"
							clip-rule="evenodd"
						></path></svg
					>
					<span class="font-semibold">Excicion Tumoral</span>
				</li>
				<li class="flex items-center space-x-3">
					<!-- Icon -->
					<svg
						class="h-5 w-5 flex-shrink-0 text-green-500 dark:text-green-400"
						fill="currentColor"
						viewBox="0 0 20 20"
						xmlns="http://www.w3.org/2000/svg"
						><path
							fill-rule="evenodd"
							d="M16.707 5.293a1 1 0 010 1.414l-8 8a1 1 0 01-1.414 0l-4-4a1 1 0 011.414-1.414L8 12.586l7.293-7.293a1 1 0 011.414 0z"
							clip-rule="evenodd"
						></path></svg
					>
					<span class="font-semibold">Esplenctomimia</span>
				</li>
				<li class="flex items-center space-x-3">
					<!-- Icon -->
					<svg
						class="h-5 w-5 flex-shrink-0 text-green-500 dark:text-green-400"
						fill="currentColor"
						viewBox="0 0 20 20"
						xmlns="http://www.w3.org/2000/svg"
						><path
							fill-rule="evenodd"
							d="M16.707 5.293a1 1 0 010 1.414l-8 8a1 1 0 01-1.414 0l-4-4a1 1 0 011.414-1.414L8 12.586l7.293-7.293a1 1 0 011.414 0z"
							clip-rule="evenodd"
						></path></svg
					>
					<span class="font-semibold">Enuclacion Ocular</span>
				</li>
				<li class="flex items-center space-x-3">
					<!-- Icon -->
					<svg
						class="h-5 w-5 flex-shrink-0 text-green-500 dark:text-green-400"
						fill="currentColor"
						viewBox="0 0 20 20"
						xmlns="http://www.w3.org/2000/svg"
						><path
							fill-rule="evenodd"
							d="M16.707 5.293a1 1 0 010 1.414l-8 8a1 1 0 01-1.414 0l-4-4a1 1 0 011.414-1.414L8 12.586l7.293-7.293a1 1 0 011.414 0z"
							clip-rule="evenodd"
						></path></svg
					>
					<span class="font-semibold">Limpieza de Oidos Profunda</span>
				</li>
			</ul>
		</div>
	</div>

	<div class="flex flex-col items-center">
		<div class="relative flex justify-center">
			<h3
				class="absolute inset-0 z-20 flex items-center justify-center text-center text-2xl text-gray-100"
				style="top: 40%;"
			>
				Estetica
			</h3>
			<PawPrint />
		</div>
		<div
			class="box mb-5 mt-4 w-72 flex-grow rounded-lg border-4 border-blue-900 bg-gray-800 p-5 text-gray-200"
		>
			<ul role="list" class="mb-8 space-y-4 text-left">
				<li class="flex items-center space-x-3">
					<!-- Icon -->
					<svg
						class="h-5 w-5 flex-shrink-0 text-green-500 dark:text-green-400"
						fill="currentColor"
						viewBox="0 0 20 20"
						xmlns="http://www.w3.org/2000/svg"
						><path
							fill-rule="evenodd"
							d="M16.707 5.293a1 1 0 010 1.414l-8 8a1 1 0 01-1.414 0l-4-4a1 1 0 011.414-1.414L8 12.586l7.293-7.293a1 1 0 011.414 0z"
							clip-rule="evenodd"
						></path></svg
					>
					<span class="font-semibold">Corte de Pelo</span>
				</li>
				<li class="flex items-center space-x-3">
					<!-- Icon -->
					<svg
						class="h-5 w-5 flex-shrink-0 text-green-500 dark:text-green-400"
						fill="currentColor"
						viewBox="0 0 20 20"
						xmlns="http://www.w3.org/2000/svg"
						><path
							fill-rule="evenodd"
							d="M16.707 5.293a1 1 0 010 1.414l-8 8a1 1 0 01-1.414 0l-4-4a1 1 0 011.414-1.414L8 12.586l7.293-7.293a1 1 0 011.414 0z"
							clip-rule="evenodd"
						></path></svg
					>
					<span class="font-semibold">Baño</span>
				</li>
				<li class="flex items-center space-x-3">
					<!-- Icon -->
					<svg
						class="h-5 w-5 flex-shrink-0 text-green-500 dark:text-green-400"
						fill="currentColor"
						viewBox="0 0 20 20"
						xmlns="http://www.w3.org/2000/svg"
						><path
							fill-rule="evenodd"
							d="M16.707 5.293a1 1 0 010 1.414l-8 8a1 1 0 01-1.414 0l-4-4a1 1 0 011.414-1.414L8 12.586l7.293-7.293a1 1 0 011.414 0z"
							clip-rule="evenodd"
						></path></svg
					>
					<span class="font-semibold">Baño Medicado</span>
				</li>
				<li class="flex items-center space-x-3">
					<!-- Icon -->
					<svg
						class="h-5 w-5 flex-shrink-0 text-green-500 dark:text-green-400"
						fill="currentColor"
						viewBox="0 0 20 20"
						xmlns="http://www.w3.org/2000/svg"
						><path
							fill-rule="evenodd"
							d="M16.707 5.293a1 1 0 010 1.414l-8 8a1 1 0 01-1.414 0l-4-4a1 1 0 011.414-1.414L8 12.586l7.293-7.293a1 1 0 011.414 0z"
							clip-rule="evenodd"
						></path></svg
					>
					<span class="font-semibold">Corte de Uñas</span>
				</li>
				<li class="flex items-center space-x-3">
					<!-- Icon -->
					<svg
						class="h-5 w-5 flex-shrink-0 text-green-500 dark:text-green-400"
						fill="currentColor"
						viewBox="0 0 20 20"
						xmlns="http://www.w3.org/2000/svg"
						><path
							fill-rule="evenodd"
							d="M16.707 5.293a1 1 0 010 1.414l-8 8a1 1 0 01-1.414 0l-4-4a1 1 0 011.414-1.414L8 12.586l7.293-7.293a1 1 0 011.414 0z"
							clip-rule="evenodd"
						></path></svg
					>
					<span class="font-semibold">Limpieza de Oidos</span>
				</li>
			</ul>
		</div>
	</div>
</div>
