<script>
	// import heroBg from './images/anna-hero-image-3.jpg';
	// import heroBg from '../../static/images/anna-hero-image-3.jpg';
	// console.log(heroBg);

	// import bg from '$images/anna-hero-image-3.jpg';
	// console.log({ bg });

	// let heroBg = './images/anna-hero-image-3.jpg';
	// console.log(heroBg);

	// bg-[url('/images/anna-hero-image-3.jpg')]

	// bg-[url{heroBg}]

	let bgImage = 'images/anna-hero-img-4.jpg';
</script>

<svelte:head>
	<title>Home Page</title>
	<meta name="description" content="Svelte homepage" />
</svelte:head>

<main
	class="hero bg-[url('/images/anna-hero-img-4.jpg')] h-screen bg-cover bg-center flex items-center justify-center relative"
>
	<div
		class="bg-white/50 backdrop-blur-md backdrop-opacity-60 mx-4 text-center text-primary py-4 md:py-12 md:px-8 rounded"
	>
		<h1 class="font-bold text-2xl md:text-6xl mb-5">Anna & Associates</h1>
		<h2 class="font-semibold text-xl md:text-3xl">
			Your Gateway to Cambodia Through Cambodian Laws Experts
		</h2>
	</div>
	<div class="text-secondary font-semibold text-base md:text-lg">
		<a
			href="/services"
			class="bg-primary duration-300 hover:bg-yellow-400 hover:text-gray-900 px-4 py-2 rounded absolute top-1/4 left-0 flex items-center w-36 justify-center"
			>Services <iconify-icon icon="ic:round-miscellaneous-services" class="ml-1" /></a
		>
		<a
			href="/partners"
			class="bg-primary duration-300 hover:bg-yellow-400 hover:text-gray-900 px-4 py-2 rounded absolute top-3/4 left-0 flex items-center w-36 justify-center"
			>Partners <iconify-icon icon="carbon:partnership" class="ml-1" /></a
		>

		<!-- <a
			href="/"
			class="bg-primary duration-300 hover:bg-yellow-400 hover:text-gray-900 px-4 py-2 rounded absolute top-1/4 right-0 flex items-center w-36 justify-center"
			><iconify-icon icon="mdi:cloud-print" class="mr-1" />Publications
		</a> -->
		<a
			href="/contact"
			class="bg-primary duration-300 hover:bg-yellow-400 hover:text-gray-900 px-4 py-2 rounded absolute top-1/4 right-0 flex items-center w-36 justify-center"
			><iconify-icon icon="material-symbols:phone-forwarded" class="mr-1" />Contact
		</a>
	</div>
</main>

<style>
	/* .hero {
		background-image: url('/images/anna-hero-img-4.jpg');
	} */
</style>
