<script>
	import { onMount } from 'svelte';
	import { pageviewCount } from '@waline/client';

	export let data;
	export let walineURL = 'https://waline-ten-hazel.vercel.app';

	onMount(async () => {
		pageviewCount({
			serverURL: walineURL,
			path: data.path

			// optional, for custom selectors, defaults to `'.waline-pageview-count'`
			// selector: 'waline-pageview-count',

			// optional, whether to increase the number of visits when fetching, the default is `true`
			// update: true,
		});
	});
</script>

<div>
	<!-- data-path will be the query condition -->
	Pageviews: <span class="waline-pageview-count" data-path={data.path} />
</div>
