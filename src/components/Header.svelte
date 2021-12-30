<script>
	export let segment;
</script>

<style lang="scss">
	@keyframes scroll {
		0% {
			bottom: 0;
		}

		100% {
			bottom: 3vh;
		}
	}

	header {
		width: 100%;
		height: 100%;
		background-image: url("/images/eyecatch.jpg");
		background-size: cover;
		background-position: 60%;
		position: relative;
		overflow: hidden;

		&::before {
			content: "";
			z-index: 2;
			display: block;
			position: absolute;
			top: 0;
			clip-path: polygon(0 0, 100% 0, 0 100%);
			background-color: $main-color;

			@include media(pc) {
				width: 100vmin;
				height: 100vmin;
			}

			@include media(smp) {
				width: 110vw;
				height: 108vh;
			}
		}

		&::after {
			content: "";
			position: absolute;
			background-color: rgba(#242B2E, 0.32);
			bottom: 0;
			left: 0;
			clip-path: polygon(0 0, 0 100%, 100% 100%);
			@include media(pc) {
				width: 120vw;
				height: 70vh;
			}

			@include media(smp) {
				width: 200vw;
				height: 70vh;
			}

		}

		.title-wrap {
			z-index: 3;
			position: relative;
			color: #fff;
			width: 100%;
			height: 100%;

			img {
				position: absolute;
				@include media(pc) {
					width: 50vmin;
					height: 50vmin;
					top: 10vmin;
					left: 10vmin;
				}
				@include media(smp) {
					width: min(70vw, 50vh);
					height: min(70vw, 50vh);
					top: 15vh;
					left: 10vw;
				}
			}

			p.tag-line {
				position: absolute;
				line-height: 2rem;

				@include media(pc){
					top: 65vmin;
					left: 10vmin;
					font-size: 3.5vmin;
				}
				@include media(smp) {
					top: min(80vw + 15vh, 55vh + 15vh);
					left: 10vw;
					font-size: min(4.5vw, 3.3vh);
					line-height: 2.6rem;
				}
			}

			&::after {
				content: "";
				z-index: 2;
				display: block;
				position: absolute;
				height: 60%;
				background-image: url("/images/scroll.svg");
				background-size: contain;
				background-repeat: no-repeat;
				background-position-y: bottom;

				@include media(pc) {
					bottom: 0;
					right: 0;
					width: calc(#{$right-bar-width} - 3vmin);
					margin-left: 1vmin;
					margin-right: 2vmin;
					margin-bottom: 1.5vmin;
				}

				@include media(smp) {
					bottom: 0;
					left: 0;
					width: 5vw;
					margin-left: 2vw;
					margin-right: 1vw;
					margin-bottom: 6vh;
				}

				animation: scroll 0.5s ease-in-out infinite alternate;
				animation-delay: 3s;
			}

		}
	}
</style>

<header>
	<div class="title-wrap">
		<h1><img src="/images/logo-square.svg" alt="ふらっとプラット"></h1>
		<p class="tag-line">
			イベントをふらっとひらく、<br>
			イベントにふらっとはいる。
		</p>
	</div>
</header>
