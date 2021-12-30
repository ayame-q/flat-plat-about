<script>
	import {getContext} from "svelte";
	import WhyDetail from "./WhyDetail.svelte";

	const {open} = getContext("simple-modal")
	const showDetail = () => {
		open(WhyDetail)
	}
</script>

<style lang="scss">
	section {
		cursor: pointer;

		@include media(pc) {
			display: flex;
			height: 90vh;
			align-items: center;
			overflow: hidden;
		}

		@include media(smp) {
			position: relative;
			height: max(80vw, 70vh);
			margin-top: 35vh;
		}

		.content-wrap {
			flex-basis: 50%;
			background-color: $main-color;
			height: 100%;
			color: #fff;
			display: flex;
			flex-direction: column;
			justify-content: space-between;
			@include media(pc) {
				padding: 10% 5%;
				padding-bottom: 2%;
			}

			@include media(smp) {
				padding: 15vh 10vw;
				padding-top: max(22vw, 15vh);
				padding-bottom: 5vh;
			}

			h2 {
				position: relative;
				font-size: 2rem;
				margin-left: 0.4rem;

				@include media(smp) {
					font-size: 6vw;
					margin-left: 0;
				}

				.why {
					display: block;
					position: absolute;
					bottom: 100%;
					left: -10%;
					transform: rotate(-25deg);
					font-size: 3.5rem;
					opacity: 0.5;


					@include media(smp) {
						font-size: 12vw;
					}
				}
			}

			ul {
				list-style-type: decimal;
				font-size: 0.9rem;
				line-height: 3.5rem;

				@include media(smp) {
					padding-left: 4.5vw;
					font-size: min(3.2vw, 2.5vh);
					line-height: min(15vw, 10vh);
				}
			}

			&::after {
				content: "";
				align-self: flex-end;
				background-size: contain;
				background-repeat: no-repeat;
				background-position: right;

				@include media(pc) {
					width: 15%;
					height: 6%;
					margin-right: 1em;
					background-image: url("/images/click-pc.svg");
				}

				@include media(smp) {
					width: 40vw;
					height: min(20vw, 20vh);
					background-image: url("/images/click-smp.svg");
				}
			}
		}

		&::before {
			content: "";
			display: block;
			flex-basis: 50%;
			background-image: url("/images/why-eyecatch.jpg");
			background-size: cover;
			background-position: left 50%;

			@include media(pc) {
				height: 150%;
			}

			@include media(smp) {
				position: absolute;
				z-index: -1;
				transform: rotate(17deg);
				background-position: left 70%;
				width: 100%;
				height: 80%;
				top: -30%;
				left: 30%;
				border: $main-color solid 5vw;
			}
		}
	}
</style>

<section on:click={showDetail}>
	<div class="content-wrap">
		<h2><span class="why">Why?</span>ふらっとプラット?</h2>
		<ul>
			<li>2020会場問題と日本の展示場</li>
			<li>COVID-19による大規模イベントの自粛要請</li>
			<li>個人向けオンライン展示会プラットフォームの現状</li>
		</ul>
	</div>
</section>
