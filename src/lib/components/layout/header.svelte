<script lang="ts">
	import { page } from '$app/state';
	import { Button } from '$lib/components';
</script>

<header class="fixed inset-0 z-100 h-[var(--header-height)] w-full backdrop-blur-[10px]">
	<div class="flex h-full w-full justify-between">
		<div class="flex h-full">
			<div class="flex flex-row gap-8 ml-10">
				<span class="relative flex items-center">Spring/Summer™</span>
			</div>
		</div>
		<nav class="flex h-full">
			<ul class="flex flex-row gap-8">
				<li class="group relative flex items-center">
					<a
						class="underline-offset-[1.5px] group-hover:underline"
						href="/ecommerce"
						aria-current={page.url.pathname.startsWith(`/ecommerce`) ? 'page' : undefined}
						>eCommerce</a
					>
				</li>
				<li class="group relative flex items-center">
					<a
						class="underline-offset-[1.5px] group-hover:underline"
						href="/websites"
						aria-current={page.url.pathname.startsWith(`/websites`) ? 'page' : undefined}
						>Websites</a
					>
				</li>
				<li class="group relative flex items-center">
					<a
						class="underline-offset-[1.5px] group-hover:underline"
						href="/approach"
						aria-current={page.url.pathname.startsWith(`/approach`) ? 'page' : undefined}
						>Approach</a
					>
				</li>
				<li class="group relative flex items-center">
					<a
						class="underline-offset-[1.5px] group-hover:underline"
						href="/join"
						aria-current={page.url.pathname.startsWith(`/journal`) ? 'page' : undefined}>Journal</a
					>
				</li>
				<li class="group relative flex items-center">
					<a
						class="underline-offset-[1.5px] group-hover:underline"
						href="/join"
						aria-current={page.url.pathname.startsWith(`/join`) ? 'page' : undefined}>Join</a
					>
				</li>
			</ul>
		</nav>
		<div class="mr-10 w-[var(--modal-width)] translate-y-[var(--header-height)]">
			<div class="relative flex flex-col gap-4 rounded border p-5">
				<p>Tell us about your project. Let’s collaborate and make great stuff.</p>
				<Button>
					{#snippet icon()}
						<svg
							stroke-linejoin="round"
							viewBox="0 0 16 16"
							style="color: hsl(var(--background-color));"
							><path
								fill-rule="evenodd"
								clip-rule="evenodd"
								d="M5.75001 2H5.00001V3.5H5.75001H11.4393L2.21968 12.7197L1.68935 13.25L2.75001 14.3107L3.28034 13.7803L12.4988 4.56182V10.25V11H13.9988V10.25V3C13.9988 2.44772 13.5511 2 12.9988 2H5.75001Z"
								fill="currentColor"
							></path></svg
						>
					{/snippet}
					Write us</Button
				>
			</div>
		</div>
	</div>
	<div
		class="mask-image pointer-events-none absolute top-full ml-10 h-5 w-[calc(100%-85px-var(--modal-width))] rounded border"
	></div>
</header>
