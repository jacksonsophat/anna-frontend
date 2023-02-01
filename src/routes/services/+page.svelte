<script>
	import { services } from './services_data';
	import { fly } from 'svelte/transition';
	import PageHeader from '../components/pageHeader.svelte';

	let isOpen = false;
	const toggle = () => (isOpen = !isOpen);

	let header = 'Services';
</script>

<svelte:head>
	<title>Our Services | Anna & Associates</title>
	<meta
		name="description"
		content="The ultimate services you need to start your business in Cambodia!"
	/>
</svelte:head>

<div class="container">
	<!-- <h1 class="text-center text-4xl font-semibold text-primary">Services</h1> -->
	<PageHeader pageHeader={'Services'} />

	<div class="grid grid-cols-1 md:grid-cols-3 my-4">
		{#each services as { id, icon, title, detail }, i}
			<!-- svelte-ignore a11y-click-events-have-key-events -->
			<div
				class="py-8 border rounded m-4 hover:bg-blue-100  hover:border-primary duration-200 cursor-pointer"
				{id}
				on:click={toggle}
			>
				<div class="text-center">
					<p class="text-6xl md:text-8xl text-primary">{@html icon}</p>
					<h2 class="text-base mt-6 font-semibold">{title}</h2>
				</div>
				{#if isOpen}
					<ul class="p-4">
						{#each detail as item}
							<li>{item}</li>
						{/each}
					</ul>
				{/if}
			</div>
		{/each}
	</div>
</div>
