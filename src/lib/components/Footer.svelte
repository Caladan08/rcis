<script lang="ts">
	import Location from 'carbon-icons-svelte/lib/Location.svelte';
	import PhoneFilled from 'carbon-icons-svelte/lib/PhoneFilled.svelte';
	import EmailNew from 'carbon-icons-svelte/lib/EmailNew.svelte';

	import LogoX from 'carbon-icons-svelte/lib/LogoX.svelte';
	import LogoFacebook from 'carbon-icons-svelte/lib/LogoFacebook.svelte';
	import LogoInstagram from 'carbon-icons-svelte/lib/LogoInstagram.svelte';
	import LogoYoutube from 'carbon-icons-svelte/lib/LogoYoutube.svelte';

	import { SvelteToast, toast } from '@zerodevx/svelte-toast';

	function copyPhoneNum(e: any) {
		navigator.clipboard.writeText(e.target?.innerHTML);
		toast.push(`<h1>Phone number copied</h1>`, {
			theme: {
				'--toastColor': 'mintcream',
				'--toastBackground': 'rgba(72,187,120,0.9)',
				'--toastBarBackground': '#2F855A',
				'--toastBorderRadius': '6px'
			}
		});
	}

	const options = {
		duration: 3000,
		initial: 1,
		next: 0,
		intro: { x: 256 }
	};
</script>

<SvelteToast {options} />

<div class="bg-red w-full p-4">
	<div class="w-full flex border-b-[1px] border-solid border-white/50">
		<div class="flex gap-48 border-r-[1px] border-solid border-white/50 p-8 w-4/6">
			<div class="flex flex-col gap-2">
				<h1 class="uppercase text-white text-2xl font-extrabold">about us</h1>
				<hr />
				<a
					href="/about/about-royale-concorde-international-school-group"
					class="text-white text-md link">About the School</a
				>
				<a href="/about/philosophy" class="text-white text-md link">Our Philosophy</a>
				<a href="/about/our-mission" class="text-white text-md link">Vision and Mission</a>
				<a href="/about/management" class="text-white text-md link">Management</a>
				<a href="/about/awards-accreditations" class="text-white text-md link">Awards and Honours</a
				>
			</div>
			<div class="flex flex-col gap-2">
				<h1 class="uppercase text-white text-2xl font-extrabold">Admissions</h1>
				<hr />
				<a href="/admission/overview" class="text-white text-md link">Overview</a>
				<a href="/admission/admission-process" class="text-white text-md link">Admission Process</a>
				<a href="/admission/faqs" class="text-white text-md link">FAQs</a>
			</div>
			<div class="flex flex-col gap-2">
				<h1 class="uppercase text-white text-2xl font-extrabold">quick links</h1>
				<hr />
				<a
					href="https://www.univariety.com/app/schoolInformation/counselling/967?year=2018"
					class="text-white text-md link">Guidance</a
				>
				<a
					href="https://www.univariety.com/app/schoolInformation/placements/967?year=2018"
					class="text-white text-md link">Placement</a
				>
				<a href="/facilities" class="text-white text-md link">Facilities</a>
				<a href="/contact-us" class="text-white text-md link">Enquire</a>
				<a href="/campus-life/co-curricular-activities" class="text-white text-md link"
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
						<span on:click={(e) => copyPhoneNum(e)}>080-25435458</span>/
						<span on:click={(e) => copyPhoneNum(e)}>080-25435459</span>/
						<span on:click={(e) => copyPhoneNum(e)}>080-25435454</span>/
						<span on:click={(e) => copyPhoneNum(e)}>080-25535455</span>/
						<span on:click={(e) => copyPhoneNum(e)}>+91 9844702444</span>/
						<span on:click={(e) => copyPhoneNum(e)}>+91 9535216115</span>
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
			<br />
			<div class="flex gap-2 items-center mb-4">
				<Location size={32} />
				<p class="font-extrabold inline text-2xl">RCIS, Chamrajpet (CBSE)</p>
			</div>
			<div class="ml-6 mb-2">
				<div class="flex gap-2 items-center">
					<PhoneFilled size={39} />
					<h1>
						<span on:click={(e) => copyPhoneNum(e)}>+91 9148820597</span>/
						<span on:click={(e) => copyPhoneNum(e)}>080-29745680</span>/
						<span on:click={(e) => copyPhoneNum(e)}>080-29744088</span>/
						<span on:click={(e) => copyPhoneNum(e)}>080-29744383</span>/
						<span on:click={(e) => copyPhoneNum(e)}>+91 9071 399 777</span>
					</h1>
				</div>
			</div>
			<div class="ml-6">
				<div class="flex gap-2 items-center">
					<EmailNew size={24} />
					<h1>inforcis07@gmail.com</h1>
				</div>
			</div>
			<br />
		</div>
	</div>
	<div class="w-full flex text-white">
		<div class="border-r-[1px] border-solid border-white/50 p-8 w-4/6">
			<div class="flex items-center gap-12 mb-4">
				<h1 class="font-extrabold text-2xl uppercase">main schools:</h1>
				<a
					href="/schools/royale-concorde-international-school-kalyan-nagar-cbse/"
					class="text-lg font-extralight link">Kalyan Nagar (CBSE)</a
				>
				<p class="text-lg font-extralight">Chamrajpet (CBSE)</p>
			</div>
			<div class="flex items-center gap-12">
				<h1 class="font-extrabold text-2xl uppercase">colleges:</h1>
				<a
					href="/schools/royale-concorde-pu-college-kalyan-nagar"
					class="text-lg font-extralight link">Kalyan Nagar, PUC (New Openings)</a
				>
				<a href="/schools/royale-concorde-pu-college-begur/" class="text-lg font-extralight link"
					>Begur, PUC (New Openings)</a
				>
			</div>
		</div>
		<div class="flex p-8 flex-col text-white w-2/6">
			<h1 class="font-extrabold text-2xl uppercase mb-2">school timing:</h1>
			<p class="ml-6">Monday - Saturday (8.00 am - 3.30 am)</p>
			<br />
			<div class="flex gap-2">
				<a
					target="_blank"
					rel="noreferrer"
					href="https://www.facebook.com/rciskalyannagarblr/?show_switched_toast=0&show_invite_to_follow=0&show_switched_tooltip=0&show_podcast_settings=0&show_community_review_changes=0&show_community_rollback=0&show_follower_visibility_disclosure=0"
				>
					<LogoFacebook size={32} class="transition-all hover:text-black" />
				</a>
				<a href="https://www.instagram.com/rciskalyannagar" target="_blank" rel="noreferrer">
					<LogoInstagram size={32} class="transition-all hover:text-black" />
				</a>
				<a href="https://twitter.com/rcischool" target="_blank" rel="noreferrer">
					<LogoX size={32} class="transition-all hover:text-black" />
				</a>
				<a
					href="https://www.youtube.com/channel/UCi0E9Xpu_t1KWaA9sPneBrg"
					target="_blank"
					rel="noreferrer"
				>
					<LogoYoutube size={32} class="transition-all hover:text-black" />
				</a>
			</div>
		</div>
	</div>
</div>

<style>
	a.link {
		position: relative;
		outline: none !important;
		transition: 0.2s;
	}
	a.link::after {
		content: '';
		background-color: black;
		position: absolute;
		bottom: 0;
		left: 0;
		height: 2px;
		width: 0;
		transition: 0.2s;
	}

	a.link:hover,
	a.link:focus {
		color: black;
	}

	a.link:hover::after,
	a.link:focus::after {
		background-color: black;
		width: 100%;
	}

	span {
		cursor: pointer;
	}
</style>
