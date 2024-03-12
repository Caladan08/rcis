<script lang="ts">
	import Search from 'carbon-icons-svelte/lib/Search.svelte';
	import Dropdown from './Dropdown.svelte';
</script>

<div class="flex justify-between px-12 py-3">
	<a href="/">
		<img src="/RCIS_Logo.png" alt="rcis logo" class="w-28" />
	</a>
	<div class="flex items-center gap-8">
		<Dropdown>
			<span slot="heading">Admission</span>
			<span slot="links">
				<a href="/admission/overview">Overview</a>
				<a href="/admission/admission-process">Admission Process</a>
				<a href="/apply-online">Apply Online</a>
				<a href="/admission/faqs">FAQs</a>
			</span>
		</Dropdown>
		<Dropdown>
			<span slot="heading">Academics</span>
			<span slot="links">
				<a href="/academics/pre-primary-level">Pre-Primary Level</a>
				<a href="/academics/primary-level">Primary Level</a>
				<a href="/academics/middle-and-secondary-level">Middle and Secondary Level</a>
				<a href="/academics/senior-secondary-level">Senior Secondary Level</a>
			</span>
		</Dropdown>
		<Dropdown>
			<span slot="heading">About</span>
			<span slot="links">
				<a href="/about/about-royale-concorde-international-school-group">About Royale Concorde International School Group</a>
				<a href="/about/philosophy">Philosophy</a>
				<a href="/about/our-mission">Our Mission</a>
				<a href="/about/management">Management</a>
				<a href="/about/why-royale-concorde-international-school">Why Royale Concorde International School</a>
				<a href="/about/awards-accreditations">Awards and Accreditations</a>
				<a href="/about/testimonials">Testimonials</a>
			</span>
		</Dropdown>
		<div>
			<a href="https://rcis.myclassboard.com/%20" target="_blank" rel="noreferrer">
				<button
					class="text-white px-6 rounded-md py-[0.7rem] border-red/60 border-2 border-solid bg-transparent hover:border-red transition-all"
					>Login</button
				>
			</a>
		</div>
		<button on:click={() => (hidden = false)} class="flex py-6"
			><Search size={24} class="hover:scale-125 hover:text-red transition-all text-white" /></button
		>
	</div>
</div>
