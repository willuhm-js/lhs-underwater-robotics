<script lang="ts">
	interface SponsorCategory {
		name: string;
		money: number;
		color: string;
		textColor?: string;
	}

	const sponsorCategories: SponsorCategory[] = [
		//planning to remake this entire page
	];
</script>

<svelte:head>
	<title>Deep Sea Tactics - Sponsors</title>
</svelte:head>

<h1>Sponsors</h1>

<main>
	{#each sponsorCategories as sponsorCategory}
		<div
			class="sponsorCategory"
			style="--color: {sponsorCategory.color}; --textColor: {sponsorCategory.textColor};"
		>
			<h2>{sponsorCategory.name} - ${sponsorCategory.money}</h2>
		</div>
	{/each}
</main>

<style>
	h1,
	h2 {
		text-align: center;
	}

	h1 {
		font-size: 6rem;
	}

	h2 {
		font-size: 3rem;
	}

	main {
		display: flex;
		flex-direction: column;
		align-items: center;
	}

	.sponsorCategory {
		background-color: var(--color);
		margin: 1rem;
		width: 800px;
		color: var(--textColor, white);
		padding: 1rem;
		border-radius: 1rem;
	}
</style>
