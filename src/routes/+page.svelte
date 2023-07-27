<script>
	import { H1 } from '$components/ui/typography/h1';
	import { H2 } from '$components/ui/typography/h2';
	import { H3 } from '$components/ui/typography/h3';
	import { H4 } from '$components/ui/typography/h4';
	import { Text } from '$components/ui/typography/Text';
	import { Button } from '$components/ui/button';
	import { cn } from '$lib/utils';
</script>

<H1>Hello</H1>
<H2>Did you know that</H2>
<H3>This is a H3?</H3>
<H4>And this is a H4</H4>
<Text>And this is a paragraph</Text>

<div class={cn('mt-6')}>
	<Button>Button</Button>
	<Button variant="secondary">Button</Button>
	<Button variant="destructive">Button</Button>
	<Button variant="outline">Button</Button>
	<Button variant="ghost">Button</Button>
	<Button variant="link">Button</Button>
</div>
