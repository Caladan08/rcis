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

<div class="min-w-[4rem] bg-[#29235c] flex justify-center">
  <button on:click={() => (hidden = false)} class="flex py-6 text-white"><Menu size={44} /></button>
</div>

<Drawer placement="right" transitionType="fly" {transitionParams} bind:hidden id="sidebar1">
	<div class="content">
		<h1>Content</h1>
	</div>
</Drawer>