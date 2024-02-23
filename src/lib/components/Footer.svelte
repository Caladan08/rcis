<div class="bg-red w-full p-12">
	<div class="w-full flex">
		<div class="flex gap-56">
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
		<div class="flex"></div>
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
