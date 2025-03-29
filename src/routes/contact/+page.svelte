<script lang="ts">
</script>

<section class="contact-section">
	<h2>Contact</h2>
	<form data-netlify="true" name="contact">
		<input type="hidden" name="form-name" value="contact" />
		<div class="form-group">
			<label for="name">Name</label>
			<input type="text" id="name" name="name" required />
		</div>
		<div class="form-group">
			<label for="email">Email</label>
			<input type="email" id="email" name="email" required />
		</div>
		<div class="form-group">
			<label for="message">Message</label>
			<textarea id="message" name="message" required></textarea>
		</div>
		<button class="button submit-button" type="submit" data-bigger>Submit</button>
	</form>
</section>