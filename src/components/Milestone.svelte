<style lang="scss">
	section {
		margin: 5.5rem 0;
		h2 {
			color: $main-color;
			font-size: 2.5rem;
			margin-left: 3rem;
			@include media(smp) {
				font-size: 7.3vw;
				margin-left: 7vw;
				margin-bottom: 5vw;
			}
		}
		p {
			@include media(smp) {
				text-align: center;
			}

			img {
				width: 93%;

				@include media(smp) {
					width: 90%;
				}
			}
		}
	}
</style>

<section>
	<h2>マイルストーン</h2>
	<p>
		<img src="/images/milestone-pc.svg" alt="マイルストーン" class="only-pc">
		<img src="/images/milestone-smp.svg" alt="マイルストーン" class="only-smp">
	</p>
</section>