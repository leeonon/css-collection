<script>
	import { cn } from '../../../utils/tw';
	import CvaButton from './components/cva-button.svelte';

	let isClick = false;

	function setClickState() {
		isClick = !isClick;
	}
</script>

<div>
	<div
		class={cn('text-red-400', {
			'text-blue-500': isClick
		})}
	>
		<h1>clsx + tailwind-merge</h1>
		<button on:click={setClickState}>onClick Change Color</button>
	</div>

	<div>
		<h1>cva</h1>
		<CvaButton>123</CvaButton>
		<CvaButton size="small" intent="secondary">123</CvaButton>
	</div>
</div>
