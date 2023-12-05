<script>
	import { init } from '@waline/client';
	import { onMount } from 'svelte';

	let containerElement;

	export let commentsURL = 'https://waline-ten-hazel.vercel.app';
	export let reactionEmojis = [
		'https://unpkg.com/@waline/emojis@1.1.0/weibo/weibo_heart_eyes.png',
		'https://unpkg.com/@waline/emojis@1.1.0/weibo/weibo_dog_joy.png',
		'https://unpkg.com/@waline/emojis@1.1.0/weibo/weibo_dog_consider.png',
		'https://unpkg.com/@waline/emojis@1.1.0/weibo/weibo_sob.png'
	];

	onMount(async () => {
		init({
			el: containerElement,
			serverURL: commentsURL,
			lang: 'en',
			reaction: reactionEmojis
		});
	});
</script>


<section id="comments">
	<div id="waline" bind:this={containerElement} />
</section>


<style>
	#comments {
		margin-top: 3rem;
	}
</style>
