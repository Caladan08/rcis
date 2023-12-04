<script lang="ts">
	import { Drawer } from "flowbite-svelte"
	import { sineIn } from 'svelte/easing';

  let hidden = true;
  let transitionParams = {
    x: 320,
    duration: 200,
    easing: sineIn
  };
</script>

<div class="flex justify-between">
	<div class="p-2">
		<img src="/RCIS_Logo.png" alt="rcis logo" class="h-28 w-[8.75rem]" />
	</div>
	<div class="p-2">
		<button on:click={() => hidden = false}>Click</button>
	</div>
</div>

<Drawer placement="right" transitionType="fly" {transitionParams} bind:hidden={hidden} id="sidebar1">
  <div class="content">
		<h1>Content</h1>
	</div>
</Drawer>