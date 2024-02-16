<script lang="ts">
	import { Carousel } from 'flowbite-svelte';
	import Navbar from '$lib/components/Navbar.svelte';
	import { fly } from "svelte/transition"

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
								transition:fly={{ y: 200, duration: 500}}
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
</div>

<style>
  :global(.carousel > div > div) {
    height: 100vh;
    border-radius: 0;
  }
</style>