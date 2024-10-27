<script>
	import Contact from '$lib/components/Contact.svelte';
	import Footer from '$lib/components/Footer.svelte';
	import List from '$lib/components/List.svelte';
	import Main from '$lib/components/Main.svelte';
	import MainNav from '$lib/components/MainNav.svelte';
</script>

<div>
	<MainNav />
</div>
<Main />
<div class="-mt-10">
	<List />
</div>
<Contact />
<Footer />

<style>
	html {
		scroll-behavior: smooth;
	}
</style>
