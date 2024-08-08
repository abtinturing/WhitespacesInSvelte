<script>
	import MyComponent from '$lib/MyComponent.svelte';
	import { mount, onMount } from 'svelte';

	onMount(() => {
		const container = document.createElement('div');
		mount(MyComponent, { target: container });

		console.warn({ innerText: container.innerText, container, innerHTML: container.innerHTML });
	});
</script>
