<script>
	import { cn } from '$lib/utils';
	import '../app.postcss';
</script>

<main class={cn('h-screen p-4 md:p-10')}>
	<slot />
</main>
