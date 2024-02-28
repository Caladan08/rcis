<script lang="ts">
	import { Drawer, Card } from 'flowbite-svelte';
	import { sineIn } from 'svelte/easing';
	import Menu from 'carbon-icons-svelte/lib/Menu.svelte';
	import Close from 'carbon-icons-svelte/lib/Close.svelte';
	import Search from 'carbon-icons-svelte/lib/Search.svelte';

	let hidden = true;
	let transitionParams = {
		x: 320,
		duration: 200,
		easing: sineIn
	};
	let searchClicked = false;
</script>

<div class="flex justify-between px-12 py-6">
	<a href="/">
		<img src="/RCIS_Logo.png" alt="rcis logo" class="w-28" />
	</a>
	<div class="flex items-center gap-8">
		<div>
			<a href="https://rcis.myclassboard.com/%20" target="_blank" rel="noreferrer">
				<button class="text-white px-6 rounded-md py-[0.7rem] bg-gradient-to-br from-red/70 to-purple/70 hover:bg-red transition-all">Login</button>
			</a>
		</div>
		<button on:click={() => (hidden = false)} class="flex py-6"
			><Menu size={49} class="hover:scale-125 hover:text-red transition-all" /></button
		>
	</div>
</div>

<Drawer
	placement="right"
	transitionType="fly"
	{transitionParams}
	bind:hidden
	id="sidebar1"
	class="bg-purple w-[28rem]"
>
	<div class="content w-full flex flex-col">
		<div class="w-full flex justify-end mb-6">
			<button on:click={() => (hidden = true)} class="text-white"><Close size={32} /></button>
		</div>
		<div class="search w-full">
			<Card
				class={`bg-black/25 w-full flex flex-row gap-4 !p-2 !px-6 max-w-lg border-black/25 border border-solid transition-all shadow-md shadow-black/25 ${
					searchClicked ? '!border-red !shadow-red/25' : ''
				}`}
			>
				<div class="flex items-center w-full">
					<Search size={24} />
					<input
						type="text"
						class="border-none bg-transparent focus:ring-0 focus:ring-offset-0 font-['Readex Pro'] text-white w-full caret-white"
						on:focusin={() => (searchClicked = true)}
						on:focusout={() => (searchClicked = false)}
						placeholder="Search..."
					/>
				</div>
			</Card>
		</div>
	</div>
</Drawer>
