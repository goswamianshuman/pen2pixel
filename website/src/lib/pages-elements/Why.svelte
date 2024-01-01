<script lang="ts">
	import { why } from '$lib/data/why'
</script>

<section class=" pb-24 md:pb-32">
	<div class="container flex items-center justify-center">
		<h2 class=" text-[32px] md:text-[40px] font-semibold">Why Pen2Pixel</h2>
	</div>
	<div class="container max-w-6xl grid grid-cols-3 items-center gap-3 mt-6">
		{#each why as data}
			<div
				class={`w-full min-h-[300px] rounded-3xl bg-gradient-to-br from-[#C220F8]/20 to-[white]/10 backdrop-filter backdrop-blur-lg px-6 py-5 ${data.span}`}
			>
				<h4 class="text-[28px] md:text-[32px] md:leading-[32px]">{data.title}</h4>
				<p
					class={`mt-4 text-[16px] font-medium text-[#C8C8C8] ${
						data.span.includes('md:col-span-3') || data.span.includes('col-span-2')
							? 'md:max-w-[80%]'
							: ''
					}`}
				>
					{data.desc}
				</p>
			</div>
		{/each}
	</div>
</section>
