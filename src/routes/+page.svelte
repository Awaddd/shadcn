<script lang="ts">
	import { H1 } from '$components/ui/typography/h1';
	import { H2 } from '$components/ui/typography/h2';
	import { H3 } from '$components/ui/typography/h3';
	import { H4 } from '$components/ui/typography/h4';
	import { Text } from '$components/ui/typography/Text';
	import { Button } from '$components/ui/button';

	import {
		Card,
		CardContent,
		CardDescription,
		CardFooter,
		CardHeader,
		CardTitle
	} from '$components/ui/card';

	const notifications = [
		{
			title: 'Your call has been confirmed.',
			description: '1 hour ago'
		},
		{
			title: 'You have a new message!',
			description: '1 hour ago'
		},
		{
			title: 'Your subscription is expiring soon!',
			description: '2 hours ago'
		}
	];
</script>

<H1>Hello</H1>
<H2>Did you know that</H2>
<H3>This is a H3?</H3>
<H4>And this is a H4</H4>
<Text>And this is a paragraph</Text>

<div class="mt-6">
	<Button>Button</Button>
	<Button variant="secondary">Button</Button>
	<Button variant="destructive">Button</Button>
	<Button variant="outline">Button</Button>
	<Button variant="ghost">Button</Button>
	<Button variant="link">Button</Button>
</div>

<Card class="w-[380px] mt-6">
	<CardHeader>
		<CardTitle>Notifications</CardTitle>
		<CardDescription>You have 3 unread messages.</CardDescription>
	</CardHeader>
	<CardContent class="grid gap-4">
		<div class="flex-1 space-y-1">
			<p class="text-sm font-medium leading-none">Push Notifications</p>
			<p class="text-sm text-muted-foreground">Send notifications to device.</p>
		</div>
		<div>
			{#each notifications as notification, i (i)}
				<div class="grid grid-cols-[25px_1fr] items-start pb-4 last:mb-0 last:pb-0">
					<span class="flex w-2 h-2 translate-y-1 rounded-full bg-sky-500" />
					<div class="space-y-1">
						<p class="text-sm font-medium leading-none">
							{notification.title}
						</p>
						<p class="text-sm text-muted-foreground">
							{notification.description}
						</p>
					</div>
				</div>
			{/each}
		</div>
	</CardContent>
	<CardFooter>
		<Button class="w-full">Cool</Button>
	</CardFooter>
</Card>
