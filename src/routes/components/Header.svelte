<script>
	const logo = './images/anna-logo-blue.png';
</script>

<header>
	<div class="bg-primary py-2 px-1 flex justify-between md:p-4">
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

	<nav class="p-4 flex justify-between items-center">
		<div>
			<a href="/">
				<img src={logo} alt="" class="w-20 md:w-32" />
			</a>
		</div>
		<div class="font-medium text-primary">
			<a href="/" class="mr-3">Home</a>
			<a href="/services" class="mr-3">Services</a>
			<a href="/about">About Us</a>
		</div>
	</nav>
</header>
