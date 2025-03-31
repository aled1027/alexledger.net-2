<script lang="ts">
</script>

<section class="contact">
	<h1 class="font-decorative">Contact</h1>
	<p class="mt-half-em">I'd love to chat with you about how I can help you grow your business.</p>
	<p>
		You can book an initial call by filling out the form below or email me: hello@alexledger.net.
	</p>
	<form class="mt-l">
		<div class="input-group">
			<label for="name">Name</label>
			<input type="text" id="name" name="name" />
		</div>
		<div class="input-group">
			<label for="email">Email</label>
			<input type="email" id="email" name="email" />
		</div>
		<div class="input-group">
			<label for="message">Message</label>
			<textarea id="message" name="message"></textarea>
		</div>
		<button class="button mt-m" type="submit">Submit</button>
	</form>
</section>

<style>
	.contact {
		max-width: var(--content-width-narrow);
		margin-inline: auto;
	}

	.contact button {
		/* Playing with fibonacci numbers for button size */
		padding-inline: 34px;
		padding-block: 21px;

		padding-inline: 21px;
		padding-block: 13px;
		font-size: var(--size-step-1);
		font-weight: var(--font-semibold);
	}

	.contact .input-group {
		display: flex;
		flex-direction: column;
		gap: var(--space-2xs);
	}
</style>
