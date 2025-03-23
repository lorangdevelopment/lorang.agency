<script lang="ts">
	import { Header } from '$lib/components';

	$effect(() => {
		document.body.style.setProperty('--theme-text-color', '14 100% 50%');
		document.body.style.setProperty('--theme-background-color', '38 71% 92%');
	});
</script>

<Header />
