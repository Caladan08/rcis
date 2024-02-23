<script>
	import Location from 'carbon-icons-svelte/lib/Location.svelte';
	import PhoneFilled from 'carbon-icons-svelte/lib/PhoneFilled.svelte';
	import EmailNew from 'carbon-icons-svelte/lib/EmailNew.svelte';
</script>

<div class="bg-red w-full p-4">
	<div class="w-full flex border-b-[1px] border-solid border-white/50">
		<div class="flex gap-48 border-r-[1px] border-solid border-white/50 p-8 w-4/6">
			<div class="flex flex-col gap-2">
				<h1 class="uppercase text-white text-2xl font-extrabold">about us</h1>
				<hr />
				<a href="/about/about-royale-concorde-international-school-group" class="text-white text-md"
					>About the School</a
				>
				<a href="/about/philosophy" class="text-white text-md">Our Philosophy</a>
				<a href="/about/our-mission" class="text-white text-md">Vision and Mission</a>
				<a href="/about/management" class="text-white text-md">Management</a>
				<a href="/about/awards-accreditations" class="text-white text-md">Awards and Honours</a>
			</div>
			<div class="flex flex-col gap-2">
				<h1 class="uppercase text-white text-2xl font-extrabold">Admissions</h1>
				<hr />
				<a href="/admission/overview" class="text-white text-md">Overview</a>
				<a href="/admission/admission-process" class="text-white text-md">Admission Process</a>
				<a href="/admission/faqs" class="text-white text-md">FAQs</a>
			</div>
			<div class="flex flex-col gap-2">
				<h1 class="uppercase text-white text-2xl font-extrabold">quick links</h1>
				<hr />
				<a
					href="https://www.univariety.com/app/schoolInformation/counselling/967?year=2018"
					class="text-white text-md">Guidance</a
				>
				<a
					href="https://www.univariety.com/app/schoolInformation/placements/967?year=2018"
					class="text-white text-md">Placement</a
				>
				<a href="/facilities" class="text-white text-md">Facilities</a>
				<a href="/contact-us" class="text-white text-md">Enquire</a>
				<a href="/campus-life/co-curricular-activities" class="text-white text-md"
					>Co-Curricular Activities</a
				>
			</div>
		</div>
		<div class="flex p-8 flex-col text-white w-2/6">
			<div class="flex gap-2 items-center mb-4">
				<Location size={32} />
				<p class="font-extrabold inline text-2xl">RCIS, Kalyan Nagar</p>
			</div>
			<div class="ml-6 mb-2">
				<div class="flex gap-2 items-center">
					<PhoneFilled size={46} />
					<h1>
						080-25435458/ 080-25435459/ 080-25435454/ 080-25535455/ +91 9844702444 / +91 9535216115
					</h1>
				</div>
			</div>
			<div class="ml-6">
				<div class="flex gap-2 items-center">
					<EmailNew size={24} />
					<h1>info@rcis.in</h1>
				</div>
			</div>
			<br />
			<br>
			<div class="flex gap-2 items-center mb-4">
				<Location size={32} />
				<p class="font-extrabold inline text-2xl">RCIS, Chamrajpet (CBSE)</p>
			</div>
			<div class="ml-6 mb-2">
				<div class="flex gap-2 items-center">
					<PhoneFilled size={39} />
					<h1>+91 9148820597/ 080-29745680/ 080-29744088/ 080-29744383/ +91 9071 399 777</h1>
				</div>
			</div>
			<div class="ml-6">
				<div class="flex gap-2 items-center">
					<EmailNew size={24} />
					<h1>inforcis07@gmail.com</h1>
				</div>
			</div>
		</div>
	</div>
</div>

<style>
	a {
		position: relative;
		outline: none !important;
		transition: 0.2s;
	}
	a::after {
		content: '';
		background-color: black;
		position: absolute;
		bottom: 0;
		left: 0;
		height: 2px;
		width: 0;
		transition: 0.2s;
	}

	a:hover,
	a:focus {
		color: black;
	}

	a:hover::after,
	a:focus::after {
		background-color: black;
		width: 100%;
	}
</style>
