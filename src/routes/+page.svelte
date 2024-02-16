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
		<div class="w-1/2 px-12 py-16">
			<h1 class="uppercase font-['Montserrat'] text-white text-4xl">
				embark on a journey of <br /> global excellence and <br />leadership at
				<b>royale <br />concorde international school</b>
			</h1>
			<br>
			<p class="font-['Montserrat'] text-white text-xl">
				Unlocking Potential Beyond the Classroom, Royale Concorde International School Fosters
				<b>Curiosity</b>, <b>Creativity</b>, and <b>Self-Belief</b>.<br><br> With a strong presence in both Bangalore and Mysore,
				we provide a forward-thinking, globally renowned education that nurtures individual talents
				and passions. Prepare for a journey of self-assuredness with us!<br><br> Our committed educators
				create an enriching learning atmosphere, promoting the expression of unique abilities and
				passions, equipping students for a journey filled with confidence in the global arena.
			</p>
		</div>
		<div class="w-1/2 flex justify-end">
			<img
				src="https://rcis.in/wp-content/uploads/2023/11/homepage-right-003c.jpg"
				alt="students studying at school"
				class="w-[35rem] h-[35rem] rounded-bl-full"
			/>
		</div>
	</div>
</div>

<style>
	:global(.carousel > div > div) {
		height: 100vh;
		border-radius: 0;
	}
	.innerShadow {
		box-shadow: 0px 10px 18px rgba(0, 0, 0, 0.4) inset;
	}
</style>