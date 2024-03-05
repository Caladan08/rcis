<script>
	import { fly } from 'svelte/transition';
	let about = false;
</script>

<!-- svelte-ignore a11y-mouse-events-have-key-events -->
<!-- svelte-ignore a11y-no-static-element-interactions -->
<div
	class="relative inline-block p-6"
	on:mouseenter={() => (about = true)}
	on:mouseleave={() => (about = false)}
>
	<h1 class="cursor-pointer text-white" on:mouse>
		<slot name="heading" />
	</h1>
	<!-- svelte-ignore a11y-no-static-element-interactions -->
	<!-- svelte-ignore a11y-mouse-events-have-key-events -->
	<div on:mouseenter={() => (about = true)} on:mouseleave={() => (about = false)}>
		{#if about}
			<div
				id="myDropdown"
				in:fly={{ y: -5, duration: 500 }}
				out:fly={{ y: -5, duration: 500 }}
				class={`dropdown-content bg-white text-sm rounded-md block absolute min-w-[160px] overflow-auto drop-shadow-2xl z-[111] mt-2`}
			>
				<slot name="links" />
			</div>
		{/if}
	</div>
</div>

<style>
	:global(.dropdown-content a) {
		color: black;
		padding: 12px 16px;
		text-decoration: none;
		display: block;
	}

	:global(.dropdown a:hover) {
		background-color: #ddd !important;
	}
</style>
