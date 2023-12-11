---
title: 'File Upload Test'
date: '2023-11-14'
updated: '2023-12-01'
categories:
  - 'sveltekit'
  - 'markdown'
  - 'svelte'
  - 'video'
coverImage: '/images/jerry-zhang-ePpaQC2c1xA-unsplash.jpg'
coverWidth: 16
coverHeight: 9
excerpt: This post demonstrates how to embed a video in a Markdown post.
---

<script>
	import Callout from '$lib/components/Callout.svelte';
    import VideoEmbed from '$lib/components/VideoEmbed.svelte'

    // video source
    let source="https://www.youtube.com/embed/KCobwAt7UA0?si=5inIyqp8AtWkFoNC"
</script>

This starter includes an `Callout.svelte` component. It's not particularly useful on its own, but here's how you might use it inside of a Markdown post, thanks to mdsvex.

<Callout>
This is an example of the Callout.svelte component! Find it in <code>src/lib/components/Callout.svelte</code>.
</Callout>

You can inject any Svelte components you want into Markdown! Just import them in a `<script>` tag and then use them wherever you like.


<VideoEmbed src={source} width={900} />


