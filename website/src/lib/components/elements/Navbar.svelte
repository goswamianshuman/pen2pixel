<script lang="ts">
	import { GithubLogo as Github } from 'radix-icons-svelte'
	import { onMount, onDestroy } from 'svelte'

	let scrollBlur = false

	onMount(() => {
		const handleScroll = () => {
			if (window.scrollY > 0) {
				scrollBlur = true
			} else {
				scrollBlur = false
			}
		}

		window.addEventListener('scroll', handleScroll)

		// Cleanup the event listener when the component is unmounted
		onDestroy(() => {
			window.removeEventListener('scroll', handleScroll)
		})
	})
</script>

<header
	class={`fixed w-full top-0 z-[99999] transition-all ease-linear duration-200 ${
		scrollBlur &&
		'bg-white/5 backdrop-filter backdrop-blur-sm firefox:bg-white/5 border-b broder-[#8C20F8]/5'
	}`}
>
	<div class="container flex items-center justify-between py-4">
		<div>
			<img src="/logo.svg" alt="" class="object-center object-fill" />
		</div>

		<div>
			<a href="/">
				<Github class="h-5 w-5" />
			</a>
		</div>
	</div>
</header>
