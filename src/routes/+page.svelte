<script lang="ts">
	import './layout.css';
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
	<main>
		<section class="px-6 py-20 sm:py-24 lg:py-28">
			<div class="mx-auto max-w-6xl">
				<div class="grid gap-12 lg:grid-cols-[1.2fr_0.8fr] lg:items-center">
					<div>
						<p class="mb-6 text-sm font-semibold tracking-[0.22em] text-[#7b685c] uppercase">
							Websites for growing businesses
						</p>
						<h1
							class="max-w-[15ch] text-5xl leading-[0.94] font-medium tracking-[-0.06em] text-[#183c34] sm:text-6xl lg:text-7xl"
							style="font-family: 'Fraunces', Georgia, serif;"
						>
							A website that makes people trust your business before they ever meet you.
						</h1>
						<p class="mt-6 max-w-xl text-lg leading-8 text-[#465b56]">
							I design and build conversion-focused websites for small businesses that want to look
							more credible, communicate value clearly, and turn more visitors into paying clients.
						</p>
						<div class="mt-8 flex flex-wrap items-center gap-4">
							<a
								href="/quote"
								class="inline-flex items-center rounded-md bg-[#183c34] px-6 py-3 text-base font-medium text-[#f7f3ee] transition hover:bg-[#123029]"
							>
								Get a free site review
							</a>
							<a
								href="#work"
								class="inline-flex items-center text-base font-medium text-[#183c34] underline decoration-[#c57b4a]/80 underline-offset-4"
							>
								See recent work
							</a>
						</div>
						<div
							class="mt-8 flex flex-wrap gap-6 border-t border-[#183c34]/15 pt-5 text-sm text-[#536760]"
						>
							<div>
								<span class="block text-xl font-semibold text-[#c57b4a]">2–4 weeks</span>
								Typical launch time
							</div>
							<div>
								<span class="block text-xl font-semibold text-[#c57b4a]">Custom</span>
								Design & build
							</div>
							<div>
								<span class="block text-xl font-semibold text-[#c57b4a]">No templates</span>
								Built for your business
							</div>
						</div>
					</div>

					<!--<div class="flex justify-center lg:justify-end">
						<div
							class="w-full max-w-md rounded-[28px] border border-[#183c34]/15 bg-[#efe4d3] p-7 shadow-[0_20px_45px_rgba(24,60,52,0.08)]"
						>
							<p class="text-xs font-semibold tracking-[0.2em] text-[#6a5c4f] uppercase">
								Built to convert
							</p>
							<div class="mt-6 space-y-5">
								<div class="rounded-2xl border border-[#183c34]/10 bg-[#f8f4ee] p-4">
									<p class="text-xs tracking-[0.18em] text-[#6a5c4f] uppercase">Trust</p>
									<p
										class="mt-2 text-2xl font-medium text-[#183c34]"
										style="font-family: 'Fraunces', Georgia, serif;"
									>
										Clear positioning
									</p>
								</div>
								<div class="rounded-2xl border border-[#183c34]/10 bg-[#f8f4ee] p-4">
									<p class="text-xs tracking-[0.18em] text-[#6a5c4f] uppercase">Clarity</p>
									<p
										class="mt-2 text-2xl font-medium text-[#183c34]"
										style="font-family: 'Fraunces', Georgia, serif;"
									>
										Stronger service messaging
									</p>
								</div>
								<div class="rounded-2xl border border-[#183c34]/10 bg-[#f8f4ee] p-4">
									<p class="text-xs tracking-[0.18em] text-[#6a5c4f] uppercase">Leads</p>
									<p
										class="mt-2 text-2xl font-medium text-[#183c34]"
										style="font-family: 'Fraunces', Georgia, serif;"
									>
										More inquiries, booked calls
									</p>
								</div>
							</div>
						</div>
					</div>-->
				</div>
			</div>
		</section>

		<section class="border-t border-[#183c34]/10 px-6 py-20">
			<div class="mx-auto max-w-6xl">
				<!--<div
					class="h-32 w-32 rounded-full bg-gradient-to-br from-[#183c34] via-[#2e534d] to-[#c57b4a] shadow-[0_18px_30px_rgba(24,60,52,0.12)]"
					aria-hidden="true"
				></div>-->
				<div>
					<p class="mb-3 text-sm font-semibold tracking-[0.18em] text-[#bf7a4d] uppercase">
						Who’s building this
					</p>
					<p class="max-w-3xl text-lg leading-8 text-[#2f403d]">
						I’m a solo designer and developer with a background in building products that people
						actually use. I write the code myself, design every layout by hand, and stay involved
						from the first conversation through launch. When you work with me, you’re working
						directly with the person building your site.
					</p>
				</div>
			</div>
		</section>

		<section class="px-6 py-20">
			<div class="mx-auto max-w-6xl">
				<h2
					class="mb-8 text-3xl font-medium tracking-[-0.04em] text-[#183c34] sm:text-4xl"
					style="font-family: 'Fraunces', Georgia, serif;"
				>
					What I build
				</h2>
				<ul class="grid gap-4 border-t border-[#183c34]/10 md:grid-cols-2">
					<li
						class="border-b border-[#183c34]/10 py-6 md:pr-6 md:[&:nth-child(odd)]:border-r md:[&:nth-child(odd)]:pr-8"
					>
						<h3
							class="text-2xl font-medium text-[#183c34]"
							style="font-family: 'Fraunces', Georgia, serif;"
						>
							Business websites
						</h3>
						<p class="mt-3 max-w-md text-base leading-7 text-[#4d5d57]">
							A clear, polished site that explains what you do and earns trust the moment someone
							lands.
						</p>
					</li>
					<li class="border-b border-[#183c34]/10 py-6 md:pl-8">
						<h3
							class="text-2xl font-medium text-[#183c34]"
							style="font-family: 'Fraunces', Georgia, serif;"
						>
							Landing pages
						</h3>
						<p class="mt-3 max-w-md text-base leading-7 text-[#4d5d57]">
							Focused pages built around a clear offer, campaign, or launch so the message feels
							obvious.
						</p>
					</li>
					<li
						class="border-b border-[#183c34]/10 py-6 md:pr-6 md:[&:nth-child(odd)]:border-r md:[&:nth-child(odd)]:pr-8"
					>
						<h3
							class="text-2xl font-medium text-[#183c34]"
							style="font-family: 'Fraunces', Georgia, serif;"
						>
							Service websites
						</h3>
						<p class="mt-3 max-w-md text-base leading-7 text-[#4d5d57]">
							A site that lays out your services and process so people know what to expect before
							they reach out.
						</p>
					</li>
					<li class="border-b border-[#183c34]/10 py-6 md:pl-8">
						<h3
							class="text-2xl font-medium text-[#183c34]"
							style="font-family: 'Fraunces', Georgia, serif;"
						>
							Launch & optimization
						</h3>
						<p class="mt-3 max-w-md text-base leading-7 text-[#4d5d57]">
							Deployment, mobile polish, speed, and the basic SEO that helps people find you online.
						</p>
					</li>
				</ul>
			</div>
		</section>

		<section id="work" class="border-t border-[#183c34]/10 px-6 py-20">
			<div class="mx-auto max-w-6xl">
				<h2
					class="text-3xl font-medium tracking-[-0.04em] text-[#183c34] sm:text-4xl"
					style="font-family: 'Fraunces', Georgia, serif;"
				>
					Recent work
				</h2>
				<p class="mt-3 max-w-2xl text-base leading-7 text-[#536760]">
					Two projects that reflect the engineering, design, and product thinking behind every site
					I build.
				</p>
				<div class="mt-8 grid gap-6 md:grid-cols-2">
					<article
						class="rounded-[24px] border border-[#183c34]/10 bg-[#efe4d3] p-7 shadow-[0_18px_30px_rgba(24,60,52,0.04)]"
					>
						<h3
							class="text-2xl font-medium text-[#183c34]"
							style="font-family: 'Fraunces', Georgia, serif;"
						>
							Stratum
						</h3>
						<p class="mt-3 text-base leading-7 text-[#425955]">
							A collaboration platform for small teams, built with auth, projects, tasks, and
							comments.
						</p>
						<a
							href="https://stratum-io.vercel.app"
							class="mt-6 inline-block text-base font-medium text-[#1d6772] underline underline-offset-4"
						>
							View the live app
						</a>
					</article>
					<article
						class="rounded-[24px] border border-[#183c34]/10 bg-[#efe4d3] p-7 shadow-[0_18px_30px_rgba(24,60,52,0.04)]"
					>
						<h3
							class="text-2xl font-medium text-[#183c34]"
							style="font-family: 'Fraunces', Georgia, serif;"
						>
							Barrel
						</h3>
						<p class="mt-3 text-base leading-7 text-[#425955]">
							An API for transforming and processing files through simple HTTP endpoints, designed
							for developers.
						</p>
						<a
							href="https://github.com/BlueOceanVale/barrel"
							class="mt-6 inline-block text-base font-medium text-[#1d6772] underline underline-offset-4"
						>
							View the code
						</a>
					</article>
				</div>
			</div>
		</section>

		<section class="border-t border-[#183c34]/10 px-6 py-20">
			<div class="mx-auto max-w-6xl">
				<h2
					class="mb-8 text-3xl font-medium tracking-[-0.04em] text-[#183c34] sm:text-4xl"
					style="font-family: 'Fraunces', Georgia, serif;"
				>
					How a project runs
				</h2>
				<ol class="space-y-6">
					<li
						class="grid gap-4 border-b border-[#183c34]/10 pb-6 md:grid-cols-[2.5rem_1fr] md:gap-6"
					>
						<span
							class="text-2xl font-medium text-[#c57b4a]"
							style="font-family: 'Fraunces', Georgia, serif;">1</span
						>
						<div>
							<h3
								class="text-xl font-medium text-[#183c34]"
								style="font-family: 'Fraunces', Georgia, serif;"
							>
								Tell me about your business
							</h3>
							<p class="mt-2 max-w-2xl text-base leading-7 text-[#4d5d57]">
								A short call or message about what you do, who you serve, and what your current site
								is missing.
							</p>
						</div>
					</li>
					<li
						class="grid gap-4 border-b border-[#183c34]/10 pb-6 md:grid-cols-[2.5rem_1fr] md:gap-6"
					>
						<span
							class="text-2xl font-medium text-[#c57b4a]"
							style="font-family: 'Fraunces', Georgia, serif;">2</span
						>
						<div>
							<h3
								class="text-xl font-medium text-[#183c34]"
								style="font-family: 'Fraunces', Georgia, serif;"
							>
								I design and build it
							</h3>
							<p class="mt-2 max-w-2xl text-base leading-7 text-[#4d5d57]">
								I turn the plan into a custom site with clear messaging, polished visuals, and
								careful feedback along the way.
							</p>
						</div>
					</li>
					<li class="grid gap-4 md:grid-cols-[2.5rem_1fr] md:gap-6">
						<span
							class="text-2xl font-medium text-[#c57b4a]"
							style="font-family: 'Fraunces', Georgia, serif;">3</span
						>
						<div>
							<h3
								class="text-xl font-medium text-[#183c34]"
								style="font-family: 'Fraunces', Georgia, serif;"
							>
								We launch it
							</h3>
							<p class="mt-2 max-w-2xl text-base leading-7 text-[#4d5d57]">
								I deploy it, polish it for mobile and speed, and hand it over ready to start
								bringing in leads.
							</p>
						</div>
					</li>
				</ol>
			</div>
		</section>

		<section class="border-t border-[#183c34]/10 px-6 py-20">
			<div
				class="mx-auto grid max-w-6xl gap-8 rounded-[28px] border border-[#183c34]/10 bg-[#f0e8dc] p-8 md:grid-cols-[1.2fr_0.8fr] md:items-center"
			>
				<div>
					<h2
						class="text-3xl font-medium tracking-[-0.04em] text-[#183c34] sm:text-4xl"
						style="font-family: 'Fraunces', Georgia, serif;"
					>
						Pricing
					</h2>
					<p class="mt-4 max-w-2xl text-base leading-7 text-[#475c57]">
						Every business is different, so every quote is too. Pricing depends on the number of
						pages, features, and how much design work is involved, but you’ll always get a clear
						number before anything starts.
					</p>
				</div>
				<a
					href="/quote"
					class="inline-flex w-fit items-center justify-center rounded-md bg-[#183c34] px-6 py-3 text-base font-medium text-[#f7f3ee] transition hover:bg-[#123029]"
				>
					Get a quote
				</a>
			</div>
		</section>

		<section class="border-t border-[#183c34]/10 px-6 py-20">
			<div class="mx-auto max-w-6xl">
				<h2
					class="mb-8 text-3xl font-medium tracking-[-0.04em] text-[#183c34] sm:text-4xl"
					style="font-family: 'Fraunces', Georgia, serif;"
				>
					Questions
				</h2>
				<dl class="grid gap-6 md:grid-cols-2">
					<div class="rounded-[20px] border border-[#183c34]/10 bg-white/50 p-6">
						<dt class="text-lg font-semibold text-[#183c34]">What does a website cost?</dt>
						<dd class="mt-2 text-base leading-7 text-[#4d5d57]">
							It depends on scope — pages, features, and custom work. You’ll get a clear quote
							before committing.
						</dd>
					</div>
					<div class="rounded-[20px] border border-[#183c34]/10 bg-white/50 p-6">
						<dt class="text-lg font-semibold text-[#183c34]">How long does it take?</dt>
						<dd class="mt-2 text-base leading-7 text-[#4d5d57]">
							Most projects finish in a few weeks, depending on scope and how quickly content comes
							together.
						</dd>
					</div>
					<div class="rounded-[20px] border border-[#183c34]/10 bg-white/50 p-6">
						<dt class="text-lg font-semibold text-[#183c34]">Do you use templates?</dt>
						<dd class="mt-2 text-base leading-7 text-[#4d5d57]">
							No. Every site is designed and built from scratch for your business.
						</dd>
					</div>
					<div class="rounded-[20px] border border-[#183c34]/10 bg-white/50 p-6">
						<dt class="text-lg font-semibold text-[#183c34]">What do you need from me?</dt>
						<dd class="mt-2 text-base leading-7 text-[#4d5d57]">
							Your content, any brand assets you have, and access to whatever services you want
							connected.
						</dd>
					</div>
				</dl>
			</div>
		</section>

		<section class="border-t border-[#183c34]/10 px-6 py-20">
			<div
				class="mx-auto max-w-4xl rounded-[28px] border border-[#183c34]/10 bg-[#183c34] p-8 text-[#f7f3ee] shadow-[0_20px_45px_rgba(24,60,52,0.18)] sm:p-10"
			>
				<h2
					class="text-3xl font-medium tracking-[-0.04em] sm:text-4xl"
					style="font-family: 'Fraunces', Georgia, serif;"
				>
					Ready for a website that works as hard as you do?
				</h2>
				<p class="mt-4 max-w-2xl text-base leading-7 text-[#dfe8e6]">
					Tell me about your business — I’ll take a look and tell you honestly what would help most.
				</p>
				<a
					href="/quote"
					class="mt-8 inline-flex items-center rounded-md bg-[#f7f3ee] px-6 py-3 text-base font-medium text-[#183c34] transition hover:bg-[#efe4d3]"
				>
					Get a free site review
				</a>
			</div>
		</section>
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
