<script lang="ts">
	import { Carousel } from 'flowbite-svelte';
	import Navbar from '$lib/components/Navbar.svelte';
	import { scale } from 'svelte/transition';
  import { quintOut } from 'svelte/easing';

	const scaleAnimation = (x) => scale(x, { duration: 500, easing: quintOut });

	const images = [
		{
			alt: 'test',
			src: 'https://rcis.in/wp-content/uploads/2023/11/banner-001-painting-1920x1080-1.jpg',
			title: 'test'
		},
		{
			alt: 'test2',
			src: 'https://rcis.in/wp-content/uploads/2023/11/banner-science-lab-1920x1080-003.jpg',
			title: 'test2'
		},
		{
			alt: 'test2',
			src: 'https://rcis.in/wp-content/uploads/2023/11/banner-001-fully-carpeted-terrace-for-sports-1920x1080-1.jpg',
			title: 'test3'
		},
		{
			alt: 'test2',
			src: 'https://rcis.in/wp-content/uploads/2023/11/banner-003-robotics-1920x1080-2.jpg',
			title: 'test4'
		},
		{
			alt: 'test2',
			src: 'https://rcis.in/wp-content/uploads/2023/11/banner-m-001-amphitheater-1920x1080-1.jpg',
			title: 'test5'
		}
	];
</script>

<div class="bg-black">
	<div class="heroSection h-screen relative bg-gradient-to-br from-red/70 to-purple/70">
		<div class="absolute top-0 left-0 z-[100] w-full">
			<Navbar />
		</div>
		<div class="carousel ">
			<Carousel {images} duration={3000} class="h-full" imgClass="rounded-[0]" transition={scaleAnimation} />
		</div>
	</div>
</div>

<style>
  :global(.carousel > div > div) {
    height: 100vh;
    border-radius: 0;
  }
</style>