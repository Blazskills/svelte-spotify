<script lang="ts">
	import LogoutButton from '$components/LogoutButton.svelte';
	import 'modern-normalize/modern-normalize.css';
	import '../styles/main.scss';
	import type { LayoutData } from './$types';
	export let data: LayoutData;

	$: user = data.user;
</script>

{#if user}
	<p>Hello {data.user?.display_name}</p>
	<LogoutButton />
{/if}

<slot />
