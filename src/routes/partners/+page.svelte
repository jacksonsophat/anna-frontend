<script>
	import PageHeader from '../components/pageHeader.svelte';
	const partners = [
		{
			id: 1,
			image: '/images/partners/1.png',
			name: 'Indochina Starfish Foundation',
			detail:
				'Our Mission: To alleviate poverty for marginalised youth through equitable access to education, healthcare, and sport.',
			link: 'https://isfcambodia.org/'
		},
		{
			id: 2,
			image: '/images/partners/2.png',
			name: 'Labor & Employment',
			detail:
				'Our Mission: To alleviate poverty for marginalised youth through equitable access to education, healthcare, and sport.',
			link: 'https://isfcambodia.org/'
		},
		{
			id: 3,
			image: '/images/partners/3.png',
			name: 'Cambodia Women Entrepreneurs Association',
			detail:
				'Successful women entrepreneurs make a meaningful impact in the economic development of Cambodia',
			link: 'http://www.cweacambodia.org/'
		},
		{
			id: 4,
			image: '/images/partners/4.png',
			name: 'Harvey Law Group',
			detail:
				'Founded in 1992 by Jean François Harvey, Harvey Law Group (HLG) has quickly evolved into a leading multinational law firm that has developed a worldwide reputation amongst discerning businesses, individuals and governments across Canada, Asia, Africa, Middle East and South America',
			link: 'https://harveylawcorporation.com/'
		},
		{
			id: 5,
			image: '/images/partners/5.png',
			name: 'AQUARii',
			detail: 'Connecting Businesses, Creating Opportunities and Growing Partnerships',
			link: 'https://aquariibd.com/'
		},
		{
			id: 6,
			image: '/images/partners/6.png',
			name: 'KhmerSME ',
			detail:
				'KhmerSME is the national digital information platform for Micro, Small and Medium Enterprises (MSMEs) of the Kingdom of Cambodia',
			link: 'https://www.khmersme.gov.kh/en/sme-taskforce/'
		},
		{
			id: 7,
			image: '/images/partners/7.png',
			name: 'Cambodia Chamber of Commerce',
			detail:
				'The Chamber of Commerce is established under the Law on Chamber of Commerce promulgated in 1995 and its relevant amendments and regulations of the Kingdom of Cambodia',
			link: 'https://www.ccc.org.kh/kh/'
		},
		{
			id: 8,
			image: '/images/partners/8.png',
			name: 'The Bar Association of the Kingdom of Cambodia',
			detail: '',
			link: 'https://bakc.org.kh/index.php/en/'
		}
	];
</script>

<main class="container">
	<PageHeader pageHeader={'Partners'} />

	<div class="grid grid-cols-1 md:grid-cols-3 my-4">
		{#each partners as { id, image, name, detail, link }, i}
			<!-- svelte-ignore a11y-click-events-have-key-events -->
			<div class="py-2 px-4 border rounded m-4  hover:border-primary hover:border-4 duration-200">
				<div class="text-center">
					<div class="h-[250px] flex items-center">
						<img class="mx-auto px-8 h-100" src={image} alt="" />
					</div>
					<h2 class="text-base mt-6 font-semibold mb-4">{name}</h2>
					<p>{detail}</p>
					<a
						class="text-sm float-right mt-4 hover:underline"
						href={link}
						target="_blank"
						rel="noreferrer">More</a
					>
				</div>
			</div>
		{/each}
	</div>
</main>

<style>
</style>
