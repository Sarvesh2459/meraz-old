<script context="module">
	export const load = async ({ params }) => ({
		props: {
			key: params.path,
		},
	});
</script>

<script>
	import Header from './_Header.svelte';
	import Sidebar from './_Sidebar.svelte';
	import Footer from './_Footer/Footer.svelte';
	import PageTransition from '$lib/components/PageTransition.svelte';
	import '../styles/main.scss';
	import Loader from './_loader.svelte'

	export let key;
</script>

<Header />
<Sidebar />
<Loader />
<PageTransition {key}>
	<slot />
</PageTransition>

<Footer />
