<script>
	import MyComponent1 from '$lib/MyComponent1.svelte';
	import MyComponent2 from '$lib/MyComponent2.svelte';
	import { mount, onMount } from 'svelte';

	onMount(() => {
		console.warn('---------------------------------');
		const expected1 = 'jshello';
		const container1 = document.createElement('div');
		mount(MyComponent1, { target: container1 });

		if (container1.innerText !== expected1) {
			console.error('Component 1 failed', {
				expected: expected1,
				got: container1.innerText,
				innerHTML: container1.innerHTML
			});
		}

		const expected2 = '```jshello```';
		const container2 = document.createElement('div');
		mount(MyComponent2, { target: container2 });

		if (container1.innerText !== expected2) {
			console.error('Component 2 failed', {
				expected: expected2,
				got: container1.innerText,
				innerHTML: container2.innerHTML
			});
		}
	});
</script>
