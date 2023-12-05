<script>
	import {init} from "@waline/client";
	import { onMount } from "svelte";

	let waline;

	onMount(async () =>{
		init({
		el: waline,
		serverURL: 'https://waline-ten-hazel.vercel.app',
		lang: 'en',
		pageview: true
	}); 
	})
	
</script>


<svelte:head>
	<title>Contact</title>
	


</svelte:head>


<h1>Contact</h1>

Reach out to us! We value your thoughts, opinions, and insights. Whether you have a news tip, a
suggestion, or simply want to express your views on a political issue, we're here to listen. Your
feedback helps us to continually improve our content and serve our readers better. Please fill out
the contact form below or email us directly. We look forward to hearing from you. Together, let's
keep the conversation about politics alive and engaging.




<form on:submit|preventDefault>
	<div class="form-section">
		<label for="name">Name</label>
		<input type="text" id="name" placeholder="Name" />
	</div>
	
	<div class="form-section">
		<label for="email">Email</label>
		<input type="email" id="email" placeholder="Email address" />
	</div>

	<div class="form-section">
	<label for="subject">Subject</label>
	<input type="text" id="subject" placeholder="Subject" />
</div>


	<div class="form-section">
	<label for="message">Message</label>
	<textarea  id="message" placeholder="What is on your mind?" />
</div>

	<input type="submit" value="Send">
</form>

<div id="waline" bind:this={waline}></div>


