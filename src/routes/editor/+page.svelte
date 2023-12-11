<!-- src/routes/+page.svelte -->

<script>
	const authorizedExtensions = ['.jpg', '.jpeg', '.png', '.webp', '.md'];
</script>

<form method="post" use:enhance enctype="multipart/form-data">
	<div class="group">
        <label for="filename">Slug Name</label>
        <input type="text" required id="filename" name="filename" />
		<label for="file">Upload your file</label>
		<input
			type="file"
			id="file"
			name="fileToUpload"
			accept={authorizedExtensions.join(',')}
			required
		/>
	</div>

	<button type="submit">Submit</button>
</form>

