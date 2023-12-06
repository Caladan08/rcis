<script lang="ts">
  import { Drawer } from 'flowbite-svelte';
	import { sineIn } from 'svelte/easing';
	import Menu from 'carbon-icons-svelte/lib/Menu.svelte';

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
	<button on:click={() => (hidden = false)} class="flex py-6 "><Menu size={32} class="hover:scale-125 hover:text-red transition-all" /></button>
</div>

<Drawer placement="right" transitionType="fly" {transitionParams} bind:hidden id="sidebar1">
	<div class="content">
		<h1>Content</h1>
	</div>
</Drawer>