<script lang="ts">
	import Navbar from '$lib/components/elements/Navbar.svelte'
	import '../styles/app.css'
	import { ModeWatcher } from 'mode-watcher'
</script>

<ModeWatcher />

<Navbar />
<slot />
