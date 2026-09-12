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

<svelte:head>
	<link rel="preconnect" href="https://fonts.googleapis.com" />
	<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin="anonymous" />
	<link
		href="https://fonts.googleapis.com/css2?family=Fraunces:opsz,wght@9..144,400;9..144,500;9..144,600&family=Inter:wght@400;500;600;700&display=swap"
		rel="stylesheet"
	/>
</svelte:head>

<div class="min-h-screen bg-[#f7f3ee] text-[#1d2d29]">
	<main class="px-6 py-16 sm:py-20">
		<div class="mx-auto max-w-5xl">
			<div
				class="rounded-[30px] border border-[#183c34]/10 bg-[#f2eee8] p-6 shadow-[0_22px_50px_rgba(24,60,52,0.06)] sm:p-10 lg:p-12"
			>
				<p class="mb-4 text-sm font-semibold tracking-[0.22em] text-[#7b685c] uppercase">
					Get a quote
				</p>
				<h1
					class="max-w-[16ch] text-4xl leading-[1.05] font-medium tracking-[-0.06em] text-[#183c34] sm:text-5xl lg:text-6xl"
					style="font-family: 'Fraunces', Georgia, serif;"
				>
					Tell me about your business
				</h1>
				<p class="mt-4 max-w-2xl text-base leading-7 text-[#4d5d57] sm:text-lg">
					A few details now saves a lot of back-and-forth later. I’ll reply personally, usually
					within a day, with either a quote or a couple of clarifying questions.
				</p>

				{#if submitted}
					<div class="mt-8 rounded-[24px] border border-[#183c34]/10 bg-[#efe4d3] p-6 sm:p-8">
						<p
							class="text-2xl font-medium text-[#183c34]"
							style="font-family: 'Fraunces', Georgia, serif;"
						>
							Thanks — that’s in my inbox.
						</p>
						<p class="mt-3 max-w-xl text-base leading-7 text-[#3d4a46]">
							I’ll get back to you within a day, usually with a quote or a couple of quick
							questions.
						</p>
					</div>
				{:else}
					<form class="mt-8 grid gap-5" onsubmit={handleSubmit}>
						<div class="grid gap-5 md:grid-cols-2">
							<label class="block">
								<span class="mb-2 block text-sm font-medium text-[#2b352f]">Your name</span>
								<input
									bind:value={name}
									required
									class="w-full rounded-xl border border-[#183c34]/15 bg-[#f8f4ee] px-4 py-3 text-base text-[#1d2d29] transition outline-none focus:border-[#183c34] focus:ring-2 focus:ring-[#183c34]/20"
								/>
							</label>

							<label class="block">
								<span class="mb-2 block text-sm font-medium text-[#2b352f]">Email</span>
								<input
									type="email"
									bind:value={email}
									required
									class="w-full rounded-xl border border-[#183c34]/15 bg-[#f8f4ee] px-4 py-3 text-base text-[#1d2d29] transition outline-none focus:border-[#183c34] focus:ring-2 focus:ring-[#183c34]/20"
								/>
							</label>
						</div>

						<label class="block">
							<span class="mb-2 block text-sm font-medium text-[#2b352f]">
								Company <em class="text-[#667772] not-italic">(optional)</em>
							</span>
							<input
								bind:value={company}
								class="w-full rounded-xl border border-[#183c34]/15 bg-[#f8f4ee] px-4 py-3 text-base text-[#1d2d29] transition outline-none focus:border-[#183c34] focus:ring-2 focus:ring-[#183c34]/20"
							/>
						</label>

						<label class="block">
							<span class="mb-2 block text-sm font-medium text-[#2b352f]">Describe the project</span
							>
							<textarea
								bind:value={description}
								required
								placeholder="What does your business do, and what do you need the site to do for you?"
								class="min-h-32 w-full rounded-xl border border-[#183c34]/15 bg-[#f8f4ee] px-4 py-3 text-base text-[#1d2d29] transition outline-none placeholder:text-[#73807b] focus:border-[#183c34] focus:ring-2 focus:ring-[#183c34]/20"
							></textarea>
						</label>

						<div class="grid gap-5 md:grid-cols-2">
							<label class="block">
								<span class="mb-2 block text-sm font-medium text-[#2b352f]">
									Estimated budget <em class="text-[#667772] not-italic">(optional)</em>
								</span>
								<input
									bind:value={budget}
									placeholder="e.g. ₹15,000–25,000"
									class="w-full rounded-xl border border-[#183c34]/15 bg-[#f8f4ee] px-4 py-3 text-base text-[#1d2d29] transition outline-none placeholder:text-[#73807b] focus:border-[#183c34] focus:ring-2 focus:ring-[#183c34]/20"
								/>
							</label>

							<label class="block">
								<span class="mb-2 block text-sm font-medium text-[#2b352f]">
									Target timeline <em class="text-[#667772] not-italic">(optional)</em>
								</span>
								<input
									bind:value={timeline}
									placeholder="e.g. within a month"
									class="w-full rounded-xl border border-[#183c34]/15 bg-[#f8f4ee] px-4 py-3 text-base text-[#1d2d29] transition outline-none placeholder:text-[#73807b] focus:border-[#183c34] focus:ring-2 focus:ring-[#183c34]/20"
								/>
							</label>
						</div>

						{#if error}
							<p class="text-sm font-medium text-[#a3402c]">{error}</p>
						{/if}

						<button
							type="submit"
							disabled={sending}
							class="inline-flex items-center rounded-md bg-[#183c34] px-6 py-3 text-base font-medium text-[#f7f3ee] transition hover:bg-[#123029] disabled:cursor-not-allowed disabled:opacity-70"
						>
							{#if sending}Sending…{:else}Send request{/if}
						</button>
					</form>
				{/if}
			</div>
		</div>
	</main>
</div>

<style>
	:global(html) {
		scroll-behavior: smooth;
	}

	:global(body) {
		background: #f7f3ee;
		color: #1d2d29;
		font-family: 'Inter', system-ui, sans-serif;
	}
</style>
