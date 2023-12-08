<script lang="ts">
	import { Drawer, GradientButton } from 'flowbite-svelte';
	import { sineIn } from 'svelte/easing';
	import Menu from 'carbon-icons-svelte/lib/Menu.svelte';
	import Close from 'carbon-icons-svelte/lib/Close.svelte';

	let hidden = true;
	let transitionParams = {
		x: 320,
		duration: 200,
		easing: sineIn
	};
</script>

<div class="flex justify-between px-12 py-6">
	<div>
		<img src="/RCIS_Logo.png" alt="rcis logo" class="w-28" />
	</div>
	<div class="flex items-center gap-8">
		<div>
			<GradientButton outline color="cyanToBlue" class="from-red to-purple">Login</GradientButton>
		</div>
		<button on:click={() => (hidden = false)} class="flex py-6"
			><Menu size={44} class="hover:scale-125 hover:text-red transition-all" /></button
		>
	</div>
</div>

<Drawer
	placement="right"
	transitionType="fly"
	{transitionParams}
	bind:hidden
	id="sidebar1"
	class="bg-purple"
>
	<div class="content w-full">
		<div class="w-full flex justify-end">
			<button on:click={() => (hidden = true)} class="text-white"><Close size={32} /></button>
		</div>
	</div>
</Drawer>
