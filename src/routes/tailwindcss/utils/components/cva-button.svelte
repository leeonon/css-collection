<script lang="ts">
	import type { HTMLButtonAttributes } from 'svelte/elements';
	import { cva, type VariantProps } from 'cva';

	const button = cva({
		variants: {
			intent: {
				primary: 'bg-blue-600 text-white',
				secondary: 'bg-red-500 text-green'
			},
			size: {
				small: 'p-2',
				medium: 'p-6'
			}
		},
		compoundVariants: [{ intent: 'primary', size: 'medium', class: 'text-read-400' }]
	});

	interface $$Props extends HTMLButtonAttributes, VariantProps<typeof button> {}

	export let intent: $$Props['intent'] = 'primary';
	export let size: $$Props['size'] = 'medium';
</script>

<button {...$$props} class={button({ intent, size, class: $$props.class })}>
	<slot />
</button>
