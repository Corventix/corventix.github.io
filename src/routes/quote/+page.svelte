<script lang="ts">
	import '../layout.css';

	let name = $state('');
	let email = $state('');
	let company = $state('');
	let budget = $state('');
	let timeline = $state('');
	let description = $state('');
	let submitted = $state(false);
	let sending = $state(false);
	let error = $state('');

	const FORMSPREE_ENDPOINT = 'https://formspree.io/f/mppzbbkr';

	async function handleSubmit(e: Event) {
		e.preventDefault();
		error = '';
		sending = true;

		const payload = {
			name,
			email,
			company,
			budget,
			timeline,
			description
		};

		try {
			const res = await fetch(FORMSPREE_ENDPOINT, {
				method: 'POST',
				headers: {
					'Content-Type': 'application/json',
					Accept: 'application/json'
				},
				body: JSON.stringify(payload)
			});

			if (res.ok) {
				submitted = true;
			} else {
				const data = await res.json().catch(() => ({}));
				error = data.error || 'Submission failed. Please try again.';
			}
		} catch (err) {
			error = 'Network error. Please try again.';
		} finally {
			sending = false;
		}
	}
</script>

<section class="px-6 py-32">
	<div class="mx-auto w-full max-w-3xl">
		<p class="mb-4 text-sm font-medium tracking-widest uppercase opacity-60">Get a quote</p>

		<h1 class="text-3xl font-bold">Tell me about your project</h1>

		{#if submitted}
			<p class="mt-6 opacity-70">Thanks! Your request has been sent. I'll get back to you soon.</p>
		{:else}
			<form class="mt-6 grid" style="gap: 20px" onsubmit={handleSubmit}>
				<div class="grid sm:grid-cols-2" style="gap: 16px">
					<input
						class="rounded-xl border px-4 py-3"
						placeholder="Your name"
						bind:value={name}
						required
					/>
					<input
						class="rounded-xl border px-4 py-3"
						type="email"
						placeholder="Email"
						bind:value={email}
						required
					/>
				</div>

				<input
					class="rounded-xl border px-4 py-3"
					placeholder="Company (optional)"
					bind:value={company}
				/>

				<textarea
					class="min-h-[120px] rounded-xl border px-4 py-3"
					placeholder="Describe the project"
					bind:value={description}
					required></textarea>

				<div class="grid gap-4 sm:grid-cols-2" style="gap: 16px">
					<input
						class="rounded-xl border px-4 py-3"
						placeholder="Estimated budget (optional)"
						bind:value={budget}
					/>
					<input
						class="rounded-xl border px-4 py-3"
						placeholder="Target timeline (optional)"
						bind:value={timeline}
					/>
				</div>

				<div>
					{#if error}
						<p class="text-red-600">{error}</p>
					{/if}

					<button
						class="mt-2 rounded-xl bg-blue-600 px-6 py-3 font-medium text-white"
						type="submit"
						disabled={sending}
					>
						{#if sending}Sending...{:else}Send request →{/if}
					</button>
				</div>
			</form>
		{/if}
	</div>
</section>
