<!--class="bg-gradient-to-b from-green-900
	to-white"-->
<script>
	import { gsap } from 'gsap';
	import { onMount } from 'svelte';
	import { ScrollTrigger } from 'gsap/dist/ScrollTrigger';

	onMount(() => {
		gsap.registerPlugin(ScrollTrigger);

		gsap.fromTo(
			'.contact__heading',
			{
				y: 100
			},
			{
				y: 0,
				ease: 'power2.inOut',
				duration: 1,
				scrollTrigger: {
					trigger: '.contact__heading',
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

<section id="horarios" class="background-contact">
	<div class="mx-auto max-w-7xl px-4 py-16 sm:px-6 lg:px-8 lg:py-20">
		<div class="contact__heading mx-auto max-w-2xl text-center lg:max-w-4xl">
			<h2
				class=" mb-4 bg-clip-text text-center text-4xl
	font-bold not-italic tracking-tight text-gray-900"
			>
				Visitanos
			</h2>
			<p class="mt-4 text-lg text-gray-500">
				Ofrecemos dos clinicas equipadas para servir a tu mascota.
			</p>
		</div>
		<div class="mt-16 lg:mt-20">
			<div class="block gap-8 md:grid md:grid-cols-2">
				<div class="mb-5 lg:mb-0">
					<div class="glass-container overflow-hidden rounded-lg">
						<!-- svelte-ignore a11y-missing-attribute -->
						<h2 class="text-center text-lg font-bold text-gray-900">Sucursal Zona Centro</h2>
						<iframe
							src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d922.5978744902841!2d-117.03095256698623!3d32.5298996449229!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x80d9390226587bd3%3A0x2e616ad93baabb07!2sGXH9%2BXR%2C%20Tijuana%2C%20B.C.%2C%20Mexico!5e1!3m2!1sen!2sus!4v1729754913511!5m2!1sen!2sus"
							width="100%"
							height="450"
							style="border:0;"
							allowfullscreen=""
							loading="lazy"
							referrerpolicy="no-referrer-when-downgrade"
						></iframe>
					</div>
					<div>
						<div class="glass-container mx-auto max-w-full overflow-hidden rounded-lg">
							<div class="px-6 py-4">
								<h3 class="text-xl font-medium text-gray-900 underline">Direccion</h3>
								<p class="mt-1 text-gray-600">
									<a
										href="https://maps.app.goo.gl/jorSa13gAPmbW8FYA"
										class="text-blue-600 hover:text-purple-900 hover:underline-offset-1"
										>Calle 7 8123-103, Zona Centro, 22534 Tijuana, B.C.</a
									>
								</p>
							</div>
							<div class="border-t border-gray-200 px-6 py-4">
								<h3 class="text-xl font-medium text-gray-900 underline">Horario</h3>
								<p class="mt-1 text-gray-600">
									<span class="font-bold">Lunes - Sabado:</span> 9am - 6pm
								</p>

								<p class="mt-1 text-gray-600">
									<span class="font-bold">Domingo: </span><span class="text-red-900"> Cerrado</span>
								</p>
							</div>
							<div class="border-t border-gray-200 px-6 py-4">
								<h3 class="text-xl font-medium text-gray-900 underline">Contactanos</h3>
								<p class="mt-1 text-gray-600">
									<span class="font-bold">Correo: </span>
									<a
										href="mailto: vet.centro@gutierrezvet.com"
										class="text-blue-600 hover:text-purple-900"
									>
										vet.centro@gutierrezvet.com
									</a>
								</p>
								<p class="mt-1 text-gray-600">
									<span class="font-bold">Telefono: </span>
									<a href="tel:+6646384164" class="text-blue-500 hover:text-purple-900">
										+664 638 4164</a
									>
								</p>
							</div>
						</div>
					</div>
				</div>
				<div>
					<div class="glass-container overflow-hidden rounded-lg">
						<h2 class="text-center text-lg font-bold text-gray-900">Sucursal Fco. Villa</h2>
						<iframe
							src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3850.89760304491!2d-117.05813742434837!3d32.50993747377642!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x80d9390226587bd3%3A0x8aff9ed074f3a4b5!2sGW5V%2BXQ%2C%20Tijuana%2C%20B.C.%2C%20Mexico!5e1!3m2!1sen!2sus!4v1729755715132!5m2!1sen!2sus"
							width="100%"
							height="450"
							style="border:0;"
							allowfullscreen=""
							loading="lazy"
							referrerpolicy="no-referrer-when-downgrade"
						></iframe>
					</div>
					<div>
						<div class="glass-container mx-auto max-w-full overflow-hidden rounded-lg">
							<div class="px-6 py-4">
								<h3 class="text-xl font-medium text-gray-900 underline">Direccion</h3>
								<p class="mt-1 text-gray-600">
									<a
										href="https://maps.app.goo.gl/EXhtjzoiqtLMMXcS6"
										class="text-blue-600 hover:text-purple-900 hover:underline-offset-1"
										>Av. Maclovio Herrera 3495, Francisco Villa, 22615 Tijuana, B.C.</a
									>
								</p>
							</div>
							<div class="border-t border-gray-200 px-6 py-4">
								<h3 class="text-xl font-medium text-gray-900 underline">Horario</h3>
								<p class="mt-1 text-gray-600">
									<span class="font-bold">Lunes - Sabado:</span> 9am - 7pm
								</p>
								<p class="mt-1 text-gray-600">
									<span class="font-bold">Domingo:</span> 9am - 2pm
								</p>

								<p class="mt-1 text-gray-600">
									<span class="font-bold">Emergencias Nocturnas: </span><span class="">
										7pm - 12am</span
									>
								</p>
							</div>
							<div class="border-t border-gray-200 px-6 py-4">
								<h3 class="text-xl font-medium text-gray-900 underline">Contactanos</h3>
								<p class="mt-1 text-gray-600">
									<span class="font-bold">Correo: </span>
									<a
										href="mailto: vet.centro@gutierrezvet.com"
										class="text-blue-600 hover:text-purple-900"
									>
										vet.centro@gutierrezvet.com
									</a>
								</p>
								<p class="mt-1 text-gray-600">
									<span class="font-bold">Telefonos:</span>
									<a href="tel:+6646377541" class="text-blue-500 hover:text-purple-900">
										+664 637 7541</a
									>,
									<a href="tel:+6646377180" class="text-blue-500 hover:text-purple-900">
										+664 637 7180</a
									>
								</p>
							</div>
						</div>
					</div>
				</div>
			</div>
		</div>
	</div>
</section>

<style>
	.background-contact {
		background-image: url('assets/contact_background.svg');
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
