<script lang="ts">
	import { GithubLogo } from 'radix-icons-svelte'
	import { Button } from '../ui/button'
</script>

<footer class="bg-gradient-to-b from-transparent to-[#050308]">
	<div class="container flex items-center justify-between py-4">
		<div>
			<img src="/logo.svg" alt="" class="object-center object-fill" />
		</div>

		<div>
			<a href="/">
				<GithubLogo class="h-5 w-5" />
			</a>
		</div>
	</div>
	<div class="container flex items-start md:items-center justify-between py-4 text-[#C8C8C8]">
		<div>
			<p class="text-[16px]">
				Project by <span class="underline text-white">Anshuman goswami</span>
			</p>
		</div>

		<div class="flex flex-col items-end md:flex-row md:items-center md:gap-10">
			<Button class="p-0" variant="link" size="sm">Privacy Policy</Button>
			<Button class="p-0" variant="link" size="sm">Terms and Condition</Button>
		</div>
	</div>
</footer>
