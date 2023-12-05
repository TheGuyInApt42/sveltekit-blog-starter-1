<script>
	import { onMount } from 'svelte';
	import { commentCount } from '@waline/client';

	export let data;
	export let walineURL = 'https://waline-ten-hazel.vercel.app';

	onMount(async () => {
		commentCount({
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
	<span data-path={data.path} class="waline-comment-count" /> comments

</div>
