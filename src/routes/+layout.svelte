<script>
	import '../app.pcss';
	import Navbar from '$lib/components/Navbar.svelte';
	import SideNavbar from '$lib/components/SideNavbar.svelte';
</script>

<div class="flex">
	<div>
		<Navbar />
		<slot />
	</div>
	<SideNavbar />
</div>

<style>
	@import url('https://fonts.googleapis.com/css2?family=Readex+Pro:wght@200;300;400;500;600;700&display=swap');
</style>
