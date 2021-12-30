<style lang="scss">
	article {
		img {
			width: 100%;
		}
	}
</style>

<article>
	{#each Array(17) as _, i}
		<p>
			<img src="/images/slides/slide{i + 1}.png" alt="スライド">
		</p>
	{/each}
</article>