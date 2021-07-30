<script>
	import Nav from '../components/Nav.svelte';
	import GoogleAnalytics from '../components/GoogleAnalytics.svelte';
	export let segment;
</script>

<GoogleAnalytics />
<Nav {segment}/>

<main>
	<slot></slot>
</main>