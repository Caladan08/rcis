<script lang="ts">
	import { Carousel } from 'flowbite-svelte';
	import Navbar from '$lib/components/Navbar.svelte';
	import { fly } from 'svelte/transition';

	const images = [
		{
			alt: 'test',
			src: 'https://rcis.in/wp-content/uploads/2023/11/banner-001-painting-1920x1080-1.jpg',
			title: 'test',
			text: "Shaping Minds,<br> Nurturing Excellence,<br> <b style='text-shadow: 2px 2px 8px #000000' class='font-[800]'>Leading the Future</b>"
		},
		{
			alt: 'test2',
			src: 'https://rcis.in/wp-content/uploads/2023/11/banner-science-lab-1920x1080-003.jpg',
			title: 'test2',
			text: "Igniting Curiosity and<br> <b style='text-shadow: 2px 2px 8px #000000' class='font-[800]'>Fueling Future Innovators</b>"
		},
		{
			alt: 'test2',
			src: 'https://rcis.in/wp-content/uploads/2023/11/banner-001-fully-carpeted-terrace-for-sports-1920x1080-1.jpg',
			title: 'test3',
			text: "Unlocking Potential,<br> Fostering Creativity,<br> <b style='text-shadow: 2px 2px 8px #000000' class='font-[800]'>Holistic Development</b>"
		},
		{
			alt: 'test2',
			src: 'https://rcis.in/wp-content/uploads/2023/11/banner-003-robotics-1920x1080-2.jpg',
			title: 'test4',
			text: "Education Beyond Boundaries,<br> <b style='text-shadow: 2px 2px 8px #000000' class='font-[800]'>Empowering Future Achievers</b>"
		},
		{
			alt: 'test2',
			src: 'https://rcis.in/wp-content/uploads/2023/11/banner-m-001-amphitheater-1920x1080-1.jpg',
			title: 'test5',
			text: "Unleashing Potential,<br> Navigating Tomorrow's<br> <b style='text-shadow: 2px 2px 8px #000000' class='font-[800]'>Unknown Challenges</b>"
		}
	];
</script>

<div class="bg-black">
	<div class="heroSection h-screen relative bg-gradient-to-br from-red/70 to-purple/70">
		<div class="absolute top-0 left-0 z-[100] w-full">
			<Navbar />
		</div>
		<div class="carousel">
			<Carousel {images} duration={3000} class="h-full" imgClass="rounded-[0]">
				<div let:Slide slot="slide" let:index class="relative">
					<Slide image={images[index]} />
					{#key index}
						<div class="absolute h-full items-end w-full flex justify-center">
							<h1
								transition:fly={{ y: 200, duration: 500 }}
								class="text-5xl leading-tight font-[300] uppercase font-['Montserrat'] mb-24 text-white text-center"
							>
								{@html images[index].text}
							</h1>
						</div>
					{/key}
				</div>
			</Carousel>
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

	:global(.carousel > div > div) {
		height: 100vh;
		border-radius: 0;
	}
	.innerShadow {
		box-shadow: 0px 10px 18px rgba(0, 0, 0, 0.4) inset;
	}
</style>