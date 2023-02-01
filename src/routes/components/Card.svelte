<!-- 3 col on Desktop and 1 col on Mb -->

<script lang="ts">
	export let id = '';
	export let image = '';
	export let name = '';
	export let detail = '';
</script>

<div
	class="py-8 border rounded m-4 hover:bg-blue-100  hover:border-primary duration-200 cursor-pointer"
	{id}
>
	<div class="text-center">
		<p class="text-6xl md:text-8xl text-primary">{image}</p>
		<h2 class="text-base mt-6 font-semibold">{name}</h2>
		<p>{detail}</p>
	</div>
</div>
