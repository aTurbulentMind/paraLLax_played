<script>
	import Svg from './insta.svelte';
	import Disco from '../lib/disco.svelte';
</script>

<div class="footer">
	<h1>Get<br />Played<br />Podcast</h1>
	<footBox>
		<ul>
			<li><a href="/">HOME</a></li>
			<li><a href="/">PODCAST</a></li>
			<li><a href="/">MERCH</a></li>
			<li><a href="/contact/">CONTACT</a></li>
			<li><a href="/about/">ABOUT</a></li>
		</ul>
	</footBox>

	<footBox>
		<socBox>
			<a href="/https://www.instagram.com/skyhigh_253/">
				<Svg />
			</a>
			<a href="/"><Disco /></a>
		</socBox>
	</footBox>
</div>
<div class="creds">
	<p>
		Get played is a production of Earwolf. The content found on this website is made out of fan
		interest and is not a representation of the Get Played podcast or Earwolf productions.
	</p>
</div>

<!-- svelte-ignore css-unused-selector -->
<style lang="scss">
	@import 'basecamp';

	.footer {
		display: grid;
		background: $gradient;
		grid-template-columns: 1fr 1fr;
		grid-template-rows: 1fr 1fr;
		z-index: 950;
		position: relative;
		text-shadow: $text_shadow;

		footBox {
			margin: 8% 0 0 0;

			h1 {
				display: grid;
				grid-row: 1;
				grid-column: 1;
				margin: $marg;
				padding: $pad;
				font-size: $f-sm;
			}

			ul {
				display: grid;
				position: relative;
				margin: 5% 3% -8% 10%;
				list-style: none;
				grid-row: 2;
				grid-column: 2;

				li {
					margin: $marg_sm;
					padding: $pad_sm;

					a {
						color: $textMain;
						font-size: $f-sm;
					}
				}
			}
			socBox {
				display: flex;
				a {
					font-size: 1vh;
					flex-direction: row;

					Svg {
						width: 2vw;
					}
				}
			}
		}

		p {
			display: grid;
			grid-row: 2;
			grid-column: 2;
			width: 100vw;
		}
	}
	.creds {
		background: $extra;
		p {
			margin-top: 0;
			margin-bottom: 0;
			text-shadow: $text_shadow;
		}
	}

	@media (min-width: 780px) {
		//foots
		.footer {
			grid-template-columns: 1fr 1fr 1fr;
			grid-template-rows: 1fr 1fr;
			margin-bottom: 0;
			footBox {
				ul {
					li {
						a {
							font-size: $f-lg;
						}
					}
				}
			}
		}
	}
</style>
