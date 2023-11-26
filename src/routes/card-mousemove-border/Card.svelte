<script>
	import { onMount, onDestroy } from 'svelte';

	/**
	 * @type {HTMLDivElement}
	 */
	let card;

	/**
	 * @param {MouseEvent} event
	 */
	function handleMouseMove(event) {
		const { clientX, clientY } = event;
		const { left, top } = card.getBoundingClientRect();
		const x = clientX - left;
		const y = clientY - top;
		card.style.setProperty('--x', `${x}px`);
		card.style.setProperty('--y', `${y}px`);
	}

	onMount(() => {
		document.addEventListener('mousemove', handleMouseMove);
	});

	onDestroy(() => {
		document.removeEventListener('mousemove', handleMouseMove);
	});
</script>

<div class="cardBox" bind:this={card}>
	<div class="card" />
</div>

<style>
	.cardBox {
		position: relative;
		--x: unset;
		--y: unset;
	}
	.cardBox::before {
		position: absolute;
		inset: -1px;
		/* z-index: -2; */
		width: calc(100% + 2px);
		height: calc(100% + 2px);
		pointer-events: none;
		content: '';
		background: radial-gradient(
			300px circle at var(--x) var(--y),
			#c33764 0,
			#6171fe 80%,
			transparent 100%
		);
		border-radius: 6px;
		transition: background 0.2s;
		contain: size;
		will-change: background;
	}
	.card {
		position: relative;
		width: 100%;
		height: 100%;
		background: rgb(34, 32, 32);
		border-radius: 6px;
		overflow: hidden;
	}
	@media (resolution >= 1.5dppx), (resolution >= 144dpi) {
  .cardBox::before {
      inset: -2px;
      width: calc(100% + 4px);
      height: calc(100% + 4px);
  }
}
</style>
