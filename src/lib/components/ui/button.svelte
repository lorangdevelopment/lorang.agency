<script lang="ts">
	let { children, icon } = $props();
</script>

<a class="group relative flex items-center gap-5" href="/">
	<span class="flex h-[25px] w-[25px] items-center rounded bg-[hsl(var(--text-color))] p-0.5">
		<span class="h-full w-full scale-70 group-hover:scale-80">
			{@render icon()}
		</span>
	</span>
	<span class="underline-offset-[1.5px] group-hover:underline">
		{@render children()}
	</span>
</a>