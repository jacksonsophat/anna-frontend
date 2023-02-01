<script lang="ts">
	import { onMount } from 'svelte';

	const logo = './images/anna-logo-blue.png';

	// let show;

	let show = true;

	// let innerWidth = window.innerWidth;

	let innerWidth: number;
	onMount(() => {
		if (innerWidth > 767) {
			show = true;
		} else {
			show = false;
		}
	});

	// if (window.innerWidth > 767.98) {
	// 	show = true;
	// } else {
	// 	show = false;
	// }

	let active = false;

	function toggle() {
		show = !show;
	}
</script>

<svelte:window bind:innerWidth />

<header>
	<div class="bg-primary py-2 px-1 flex  justify-between md:p-4">
		<div class="text-white">
			<a
				href="https://www.facebook.com/annaassociatess"
				target="_blank"
				class="text-lg"
				rel="noreferrer"
			>
				<iconify-icon icon="ri:facebook-box-fill" />
			</a>

			<a
				href="https://www.linkedin.com/company/anna-associates/"
				target="_blank"
				class="text-lg"
				rel="noreferrer"
			>
				<iconify-icon icon="mdi:linkedin" />
			</a>

			<a href="mailto:info@anna-associates.com" class="text-lg">
				<iconify-icon icon="material-symbols:mail-rounded" />
			</a>
		</div>
		<div class="text-white">
			<small class="mr-2">Email: info@anna-associates.com</small>
			<a href="tel:+12273012">
				<small class="border rounded px-2 py-1">
					<i class="fa-solid fa-phone-arrow-right" /> +12 273 012</small
				>
			</a>
		</div>
	</div>

	<nav class="p-4 flex justify-between items-center flex-wrap">
		<div>
			<a href="/">
				<img src={logo} alt="" class="w-14 md:w-24" />
			</a>
		</div>
		<button
			class="md:hidden border rounded p-2 flex items-center"
			class:active
			on:click={toggle}
			on:click={() => (active = !active)}
		>
			<iconify-icon icon="ci:hamburger" class="text-primary text-base " />
		</button>

		{#if show}
			<div
				class="font-medium text-primary w-full block flex-grow md:flex md:items-center md:w-auto py-4 text-center bg-blue-100 md:bg-transparent mt-4 md:mt-0 rounded md:justify-end"
			>
				<a href="/" class="mr-3 block">Home</a>
				<a href="/services" class="mr-3 block">Services</a>
				<a href="/about" class="mr-3 block">About Us</a>
				<a href="/partners" class="mr-3 block">Partners</a>
				<a href="/contact" class="block">Contact Us</a>
			</div>
		{/if}
	</nav>
</header>

<style>
	.active {
		background-color: #eff6ff;
	}
</style>
