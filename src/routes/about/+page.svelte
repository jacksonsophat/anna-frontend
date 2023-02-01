<script>
	import { each } from 'svelte/internal';
	import { people } from './people_data';

	let showDetail = false;

	function toggle() {
		showDetail = !showDetail;
	}

	console.log(people[0].detail);
</script>

<div>
	<section class="bg-[url('/images/bg/bg-1.png')] p-6 md:p-12">
		<div
			class="text-white bg-black/25 p-4 md:p-8 rounded md:flex text-center md:text-left container"
		>
			<h2 class="text-xl font-semibold mb-4  md:w-1/3">Our Mission</h2>
			<p>
				Lorem ipsum dolor sit amet consectetur adipisicing elit. Aliquam deserunt impedit
				exercitationem atque necessitatibus voluptas consequatur nobis consectetur ipsam rerum
				magnam sequi debitis ut, eius temporibus error corrupti beatae. Aliquid.
			</p>
		</div>
	</section>
	<!-- About Us -->
	<section class="mt-8">
		<div class="bg-primary text-white text-xl font-semibold  py-4 md:p-10 mb-6">
			<h2 class="container">About Us</h2>
		</div>
		<div class="container">
			<p>
				<span class="font-bold">Anna &amp; Associates (“ANNA”)</span> is an independent, full-service
				law firm registered with the Bar Association of the Kingdom of Cambodia.
			</p>
			<br />
			<p>
				ANNA is founded with the solid mission that each service that we provide must come from our
				high commitment to producing high quality works to our client with professionalism, so that
				this is the only way that we can earn trust from our client, and to meet our client’s
				objective. We prioritize each work that we do is to meet the high expectation of our clients
				who are not only international clients but also local clients
			</p>
			<br />
			<p>
				With ANNA, clients will get advantage not only the legal knowledge in-depth of rules and
				regulations but not also very practical advice to fit into each business of our clients.
				Under ANNA, there two big practice group as following:
			</p>
			<br />
			<ol class="list-decimal pl-6">
				<li>
					COMMERCIAL PRACTICE GROUP covers all matters related to corporate, banking and finance,
					fintech, labor &amp; employment, real estates &amp; construction, commercial contract
					&amp; business licensing, and corporate governance and compliance; and
				</li>
				<li>
					COMMERCIAL LITIGATION PRACTICE GROUP covers any disputes related to commercial contracts,
					real estates investment structures, loan recovery and labor disputes between employer and
					employee, that need to be resolved with alternative disputes resolutions via negotiation,
					mediation and arbitration before stepping into any competent courts of the Kingdom.
				</li>
			</ol>
			<br />
			<p>
				With ANNA, we are pride and proud to claim that each practice group is composed with highly
				skilled, trained and experienced professional, whom always come up with their expertise and
				professionalism.
			</p>
			<br />
			<p>
				With ANNA’s mission and commitment, we are not only assisting clients to start up their
				business(es) with well structures to be complied with rules and regulations, but also to
				provide every support in each business operations, expansion, new alerts of any regulations
				that can impact our clients and to defense clients in each stage of dispute level either
				outside of court room or inside of court room. We are proud to provide from end to end
				process of our client’s business life.
			</p>
			<br />
			<p>
				With ANNA, we aim very high to protect our clients and to support our client’s in every
				circumstance, every business operation without any hesitation. We always go with our client.
				&nbsp;&nbsp;
			</p>
		</div>
	</section>
	<!-- End About Us -->
	<section class="mt-8">
		<div>
			<div class="bg-primary text-white text-xl font-semibold  py-4 md:p-10 mb-6">
				<h2 class="container">Our People</h2>
			</div>

			<div class="container">
				<div class="md:flex gap-4 mb-8 justify-center">
					<div class="bg-gray-100 p-2 rounded mb-4">
						<img src="/images/people/lina.png" alt="" />
						<div class="py-2">
							<h5 class="font-semibold text-xl mb-2">Ms. Sophat Chanleakhena</h5>
							<p>Founder and the Managing Partner</p>
						</div>
					</div>
					<div class="bg-gray-100 p-2 rounded">
						<img src="/images/people/esrra.png" alt="" />
						<div class="py-2">
							<h5 class="font-semibold text-xl mb-2">Mr. Beng Born Essra</h5>
							<p>Co-founder and Manager of Tax</p>
						</div>
					</div>
					<div />
				</div>
				<!-- Employee -->
				<div class="grid grid-cols-1 md:grid-cols-3 gap-4">
					{#each people as { name, title, image, detail }, i}
						<button class="bg-gray-100 rounded p-2 flex flex-col" on:click={toggle}>
							<img src={image} alt={name} class="w-full m-0" />
							<div class="mt-2">
								<h5 class="font-semibold text-xl mb-2">{name}</h5>
								<p>{title}</p>
							</div>
							{#if showDetail}
								<hr class="my-2" />
								<div class="text-left mt-2 text-sm">
									{#each detail as item, i}
										<p class="mb-4">
											{item}
										</p>
									{/each}
								</div>
							{/if}
						</button>
					{/each}
				</div>
			</div>
		</div>
	</section>
</div>
