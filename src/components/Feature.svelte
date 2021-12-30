<style lang="scss">
	article {
		section {
			margin: 10vh 10vw;

			min-height: min(90vh, 90vw / 16 * 9);
			display: flex;
			flex-direction: column;
			justify-content: center;

			h2 {
				color: $title-color;
				width: fit-content;
				min-width: 57vw;
				margin-left: -10vw;
				margin-top: 4em;
				margin-bottom: 2em;
				font-size: 1.5rem;
				padding: 1.5em;
				padding-left: 10vw;
				background-color: $main-color;
				position: relative;
				@include media(pc) {
					padding-right: 3em;
				}

				@include media(smp) {
					font-size: 5.8vw;
					padding-right: 10vw;
				}

				&::before {
					content: "";
					position: absolute;
					display: block;
					width: 60%;
					height: 100%;
					transform: rotate(-17deg);
					background-color: $main-color;
					bottom: 20%;
					left: -10%;
					z-index: -1;
				}
			}

			.content-wrap {
				display: flex;
				flex-direction: row;

				@include media(smp) {
					flex-direction: column-reverse !important;
				}

				.mockup {
					@include media(pc) {
						flex-basis: 48%;
						margin-left: 2%;
					}

					@include media(smp) {
						margin: 3rem 0;
					}

					img {
						width: 90%;
					}
				}

				.text-wrap {
					display: flex;
					flex-direction: column;
					flex-basis: 50%;
					@include media(pc) {
						font-size: 0.8rem;
					}
					@include media(smp) {
						margin: 3rem 0;
						margin-top: 0;
					}

					p {
						margin: 0.8em 0;

						@include media(smp) {
							font-size: 3.3vw;
							line-height: 6.4vw;
						}
					}

					.key-sentence {
						@include media(pc){
							font-size: 1.2rem;
						}

						@include media(smp) {
							font-size: 4.5vw;
							line-height: 9.5vw;
						}
					}
				}
			}

			&:nth-child(2n) {
				align-items: flex-end;

				h2{
					margin-left: auto;
					margin-right: -10vw;
					padding-right: 10vw;

					@include media(pc) {
						padding-left: 3em;
					}

					&::before{
						transform: rotate(17deg);
						left: auto;
						right: -10%;
					}
				}

				.content-wrap{
					flex-direction: row-reverse;

					.text-wrap{

					}
				}

				.mockup {
					@include media(pc) {
						margin-left: auto;
						margin-right: 2%;
					}
				}
			}

		}
	}

</style>

<main>
	<article>
		<section>
			<h2>いつでもふらっと。<br class="only-smp">でも、圧倒的体験感</h2>
			<div class="content-wrap">
				<div class="text-wrap">
					<p class="key-sentence">
						オンラインでも感じられる<br>
						イベントの”賑やかさ”、”楽しさ”
					</p>
					<p>
						イベントで人が集まっている賑やかさや、<br class="only-smp">楽しさを感じられる<br class="only-pc">たくさんの参加者の動きと<br class="only-smp">わいわい話せるチャット<br>
						さらに賑やかな空間を感じられる、<br class="only-smp">上下左右に広く広がる会場マップ
					</p>
				</div>
				<p class="mockup"><img src="images/mockup-top.png" alt=""></p>
			</div>
		</section>
		<section>
			<h2>誰でもふらっと。<br class="only-smp">今すぐイベント開催</h2>
			<div class="content-wrap">
				<div class="text-wrap">
					<p class="key-sentence">
						個人1人からでも、驚くほど簡単に<br>
						展示会を主催できる<br class="only-smp">オンラインイベントスペース<br>
						え？今日やりたい？大丈夫です。
					</p>
					<p>
						イベントの開催はトップページから、<br class="only-smp">必要な情報を入力するだけ<br>
						誰でも簡単に、いつでもイベントを主催できる<br>
						資料請求などの面倒なステップは一切ありません。
					</p>
				</div>
				<p class="mockup"><img src="images/mockup-make-event.png" alt=""></p>
			</div>
		</section>
		<section>
			<h2>出展もふらっと。<br class="only-smp">ブースにはあなたの個性を</h2>
			<div class="content-wrap">
				<div class="text-wrap">
					<p class="key-sentence">
						誰でも、自分の世界を<br>
						すぐに作れます
					</p>
					<p>
						出展はイベントページから、<br class="only-smp">必要な情報を入力するだけ<br>
						作品の配置や雰囲気など<br>
						ブースは自由にカスタマイズして<br>
						あなたを表現できます<br>
					</p>
				</div>
				<p class="mockup"><img src="images/mockup-make-booth.png" alt=""></p>
			</div>
		</section>
	</article>
</main>