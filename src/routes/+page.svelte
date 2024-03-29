<script lang="ts">
	import Navbar from '$lib/components/Navbar.svelte';
	import { fly } from 'svelte/transition';
</script>

<svelte:head>
	<title
		>Royale Concorde International School | Premium CBSE School in Bangalore, Nurturing Holistic
		Education</title
	>
</svelte:head>

<div>
	<div class="heroSection h-screen bg-cover">
		<div>
			<Navbar />
		</div>
		<div class="w-full flex justify-center flex-col gap-4 px-44 pt-24">
			<h1
				transition:fly={{ y: 200, duration: 500 }}
				class="text-[3.5rem] leading-tight font-[250] uppercase font-['Montserrat'] text-white text-left"
			>
				Education Beyond Boundaries,<br />
				<b style="text-shadow: 2px 2px 8px #000000" class="font-[800]"
					>Empowering Future Achievers</b
				>
			</h1>
			<p class="text-white text-xl max-w-4xl">
				Discover a transformative educational journey at RCIS, where academic excellence meets
				holistic development, shapign tomorrow's leaders
			</p>
			<li class="content__item z-[1] list-none mt-2">
				<button class="button button--pandora relative text-white"><span>Join Us</span></button>
			</li>
		</div>
	</div>
	<div class="flex bg-[url('/SectionTwoBG.svg')] bg-cover bg-center innerShadow">
		<div class="w-1/2 p-12">
			<h1 class="uppercase text-white text-4xl">
				embark on a journey of <br /> global excellence and <br />leadership at
				<b>royale <br />concorde international school</b>
			</h1>
			<br />
			<p class="text-white text-xl">
				Unlocking Potential Beyond the Classroom, Royale Concorde International School Fosters
				<b>Curiosity</b>, <b>Creativity</b>, and <b>Self-Belief</b>.<br /><br /> With a strong
				presence in both Bangalore and Mysore, we provide a forward-thinking, globally renowned
				education that nurtures individual talents and passions. Prepare for a journey of
				self-assuredness with us!<br /><br /> Our committed educators create an enriching learning atmosphere,
				promoting the expression of unique abilities and passions, equipping students for a journey filled
				with confidence in the global arena.
			</p>
		</div>
		<div class="w-1/2 flex justify-center items-center">
			<div class="bounce h-full w-full flex items-center justify-center">
				<img
					src="https://rcis.in/wp-content/uploads/2023/11/homepage-right-003c.jpg"
					alt="students studying at school"
					class="w-[35rem] h-[35rem] rounded-full border-2 border-dashed border-red"
				/>
			</div>
		</div>
	</div>
	<div class="w-full flex justify-center bg-[#0d0d0d] p-12">
		<div class="flex gap-4">
			<a href="/facilities">
				<div
					class="flex flex-col justify-end hover:bg-[#262626] bg-[#171717] transition-all rounded-lg facilityOne hover:scale-[1.02] p-6"
				>
					<h1 class="text-2xl font-bold text-white">Facilities</h1>
				</div>
			</a>
			<a href="/admission/overview">
				<div
					class="flex flex-col justify-end hover:bg-[#262626] bg-[#171717] transition-all rounded-lg facilityTwo hover:scale-[1.02] p-6"
				>
					<h1 class="text-2xl font-bold text-white">Admissions</h1>
				</div>
			</a>
			<a href="/campus-life/extra-curricular-activities">
				<div
					class="flex flex-col justify-end hover:bg-[#262626] bg-[#171717] transition-all rounded-lg facilityThree hover:scale-[1.02] p-6"
				>
					<h1 class="text-2xl font-bold text-white">Sports Infrastructure</h1>
				</div>
			</a>
		</div>
	</div>
	<div class="p-12 w-full bg-white">
		<div class="w-full flex items-center flex-col gap-10">
			<h1 class="text-4xl font-bold">Our accomplishments stand as evidence</h1>
			<div class="numbers w-full flex justify-evenly cursor-default">
				<div class="flex flex-col">
					<h1 class="font-extralight text-6xl">20</h1>
					<h1>Years of Excellence</h1>
				</div>
				<div class="flex flex-col">
					<h1 class="font-extralight text-6xl">20000+</h1>
					<h1>Students</h1>
				</div>
				<div class="flex flex-col">
					<h1 class="font-extralight text-6xl">600+</h1>
					<h1>Staff & Teachers</h1>
				</div>
				<div class="flex flex-col">
					<h1 class="font-extralight text-6xl">15L sq.ft</h1>
					<h1>Campus Area</h1>
				</div>
			</div>
		</div>
	</div>
	<div class="p-12 bg-[url('/SneakPeek.svg')] bg-cover">
		<div>
			<div class="container flex">
				<div class="card">
					<img src="https://rcis.in/wp-content/uploads/2023/09/Sneak-Peek-08.jpg" alt="" class="w-full h-auto object-cover" />
				</div>
				<div class="card">
					<img src="https://rcis.in/wp-content/uploads/2023/09/Sneak-Peek-01.jpg" alt="" class="w-full h-auto object-cover" />
				</div>
				<div class="card">
					<img src="https://rcis.in/wp-content/uploads/2023/10/sneakpeak-004a.jpg" alt="" class="w-full h-auto object-cover" />
				</div>
				<div class="card">
					<img src="https://rcis.in/wp-content/uploads/2023/09/Sneak-Peek-02.jpg" alt="" class="w-full h-auto object-cover" />
				</div>
				<div class="card">
					<img src="https://rcis.in/wp-content/uploads/2023/09/Sneak-Peek-05.jpg" alt="" class="w-full h-auto object-cover" />
				</div>
				<div class="card">
					<img src="https://rcis.in/wp-content/uploads/2023/09/Sneak-Peek-07.jpg" alt="" class="w-full h-auto object-cover" />
				</div>
			</div>
			<h1 class="uppercase font-light text-white text-5xl text-left mt-12">
				take a sneak peek at <b class="font-bold">royale concorde international school</b>
			</h1>
		</div>
	</div>
</div>

<style>
	p,
	h1 {
		font-family: Montserrat;
	}

	.facilityOne,
	.facilityTwo,
	.facilityThree {
		width: 450px;
		height: 350px;
		background-size: cover;
	}

	.facilityOne {
		background-image: linear-gradient(to bottom, rgba(0, 0, 0, 0), rgba(0, 0, 0, 0.6)),
			url('https://rcis.in/wp-content/uploads/2023/09/Facilities-01.jpg');
	}
	.facilityTwo {
		background-image: linear-gradient(to bottom, rgba(0, 0, 0, 0), rgba(0, 0, 0, 0.6)),
			url('https://rcis.in/wp-content/uploads/2023/09/Admissions-01.jpg');
	}
	.facilityThree {
		background-image: linear-gradient(to bottom, rgba(0, 0, 0, 0), rgba(0, 0, 0, 0.6)),
			url('https://rcis.in/wp-content/uploads/2023/09/Sports-Infrastructure-01.jpg');
	}
	:global(.sneakPeek > div > div) {
		height: 32rem;
		border-radius: 0;
	}
	.innerShadow {
		box-shadow: 0px 10px 18px rgba(0, 0, 0, 0.4) inset;
	}

	.heroSection {
		background-image: linear-gradient(to top, rgba(0, 0, 0, 0), rgba(0, 0, 0, 0.8)),
			url('https://rcis.in/wp-content/uploads/2023/10/Independence-Day-2023-24-new-006.jpg');
	}

	.button::before,
	.button::after {
		position: absolute;
		top: 0;
		left: 0;
		width: 100%;
		height: 100%;
	}

	.button--pandora {
		background: #d60202;
		font-weight: 700;
		padding: 0;
		border-radius: 5px;
	}

	.button--pandora span {
		display: block;
		background: #d55a5a;
		padding: 1.25rem 2rem;
		border: 0.5px solid #d60202;
		border-radius: 5px;
		transform: translate3d(-4px, -4px, 0);
		transition: transform 0.3s cubic-bezier(0.7, 0, 0.2, 1);
	}

	.button--pandora:hover span {
		transform: translate3d(-8px, -8px, 0);
	}

	.card {
		display: flex;
		height: 490px;
		width: 600px;
		background-color: #17141d;
		border-radius: 10px;
		box-shadow: -1rem 0 3rem #000;
		transition: 0.4s ease-out;
		position: relative;
		left: 0px;
	}

	.card:not(:first-child) {
		margin-left: -50px;
	}

	.card:hover {
		transform: translateY(-20px);
		transition: 0.4s ease-out;
	}

	.card:hover ~ .card {
		position: relative;
		left: 50px;
		transition: 0.4s ease-out;
	}
</style>
