<script>
	export let name;
	import Countdown from 'svelte-countdown/src/index.js';
</script>

<main>
	<h1>Cottaging:Resurrection</h1>
	<Countdown from="2022-04-07 08:00:00" dateFormat="YYYY-MM-DD H:m:s" zone="Europe/London" let:remaining>
		<div class="whatever">
			{#if remaining.done === false}
			<!-- <span>{remaining.years} years</span>
			<span>{remaining.months} months</span>
			<span>{remaining.weeks} weeks</span> -->
			<span>{remaining.months} months</span>
			<span>{remaining.days} days</span>
			<span>{remaining.hours} hours</span>
			<span>{remaining.minutes} minutes</span>
			<span>{remaining.seconds} seconds</span>
			{:else}
			<h2>The time has come!</h2>
			{/if}
		</div>
	</Countdown>
</main>

<style>
	main {
		background-color: #282c34;
		min-height: 100vh;
		display: flex;
		flex-direction: column;
		align-items: center;
		justify-content: center;
		font-size: calc(10px + 2vmin);
		color: white;
	}

	h1 {
		color: #00ff4c;
		text-transform: uppercase;
		font-size: 1em;
		font-weight: 100;
		align-items: center;
	}

	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}
</style>