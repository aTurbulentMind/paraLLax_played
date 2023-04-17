<body>
	<box class="main"
		><p>
			That fellow gamer turned out to be my future co-host on the Get Played podcast. We bonded over
			our mutual love for gaming and our knack for sarcasm. We decided to channel our passion into a
			podcast where we could share our brutally honest opinions on the latest games, discuss gaming
			news and trends, and poke fun at the gaming industry's quirks and shortcomings.
		</p>
		<p>
			As our podcast grew in popularity, we landed interviews with game developers, attended gaming
			conventions, and even got invited to be guest judges on a gaming reality show. Our sarcastic
			and dry first-person tone became our trademark, and we reveled in our role as the
			self-appointed "voice of reason" in the gaming community.
		</p>
	</box>

	<!--card-->
	<div class="l_r__block">
		<img src="img/h_ent.png" alt="" />
		<div class="l_r__title"><h2>Heather <br /> Campbell</h2></div>

		<div class="l_r__body">
			<p>
				Lorem ipsum, dolor sit amet consectetur adipisicing elit. Laboriosam animi reprehenderit vel
				nulla, soluta impedit.
			</p>

			<a href="/about/heather/">Learn More</a>
		</div>
	</div>
	<!--end-->

	<!--card-->
	<div class="l_r__block_l">
		<img class="img_l" src="img/m_ent.png" alt="" />
		<div class="l_r__title_l"><h2>Matt <br /> Apadoca</h2></div>

		<div class="l_r__body_l">
			<p>
				Lorem ipsum, dolor sit amet consectetur adipisicing elit. Perferendis voluptate odio facilis
				ducimus aliquam quo distinctio natus quidem neque nemo?
			</p>

			<a href="/about/matt/">Learn More</a>
		</div>
	</div>
	<!--end-->

	<!--card-->
	<div class="l_r__block">
		<img class="img" src="img/n_ent.png" alt="" />
		<div class="l_r__title"><h2>Nick <br /> Wiger</h2></div>

		<div class="l_r__body">
			<p>
				Lorem ipsum dolor sit, amet consectetur adipisicing elit. Rerum aliquam molestias facilis
				autem doloremque. Adipisci, amet soluta reprehenderit atque excepturi
			</p>

			<a href="/about/nick/">Learn More</a>
		</div>
	</div>
	<!--end-->
</body>

<!-- svelte-ignore css-unused-selector -->
<style lang="scss">
	@import '../src/lib/basecamp';
	body {
		margin-top: 4rem;
		scroll-behavior: smooth;
		transition: transform 0.2s ease-in-out;
		margin-bottom: 1px;
	}

	.box {
		--size: 300px;
		height: fit-content;
		width: 100vw;
		background: $backMain;
		align-content: center;

		a {
			p {
				align-content: center;
				font-size: $f-lg;
				margin: 5vh 25vw;
			}
		}
	}

	//l_r_leted work block

	.l_r__block,
	.l_r__block_l {
		margin: $full_marg;
	}

	.l_r__block,
	.l_r__block_l {
		.l_r__body,
		.l_r__body_l {
			a {
				margin: $full_marg;
			}
		}
	}

	@media only screen and (min-width: 780px) {
		.l_r__block,
		.l_r__block_l {
			margin: 10vh 5vw;
		}
	}
</style>
