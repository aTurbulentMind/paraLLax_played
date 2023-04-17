<script lang="ts">
	let scroll!: number;
	if (typeof window !== 'undefined') {
		scroll = window.scrollY;
	}
</script>

<svelte:window bind:scrollY={scroll} />
<body>
	<section>
		<div class="box main">
			<img src="../img/matt_A.jpg" alt="" />
			<p>
				Matt Apodaca's journey to becoming the co-host of the wildly popular "Get Played" podcast
				all started with his love for video games. Ever since he was a kid, Matt had a deep passion
				for gaming. From spending hours perfecting his skills on his favorite consoles to staying up
				late playing online with friends, gaming was his ultimate escape and source of joy. Little
				did he know that his childhood hobby would one day turn into a full-blown podcast that would
				capture the hearts of gamers around the world!
			</p>
			<p>
				As Matt grew older, his love for gaming never wavered. He found himself constantly
				discussing the latest game releases, debating gaming strategies, and sharing his gaming
				experiences with anyone who would listen. His friends and family often joked that he had a
				"PhD in Gaming" because of his extensive knowledge and enthusiasm for the subject. Matt's
				witty sense of humor and entertaining storytelling skills made his gaming anecdotes a hit at
				parties and gatherings, and soon enough, he realized he had a knack for entertaining others
				with his gaming-related banter.
			</p>
			<p>
				One fateful day, Matt crossed paths with his fellow gaming enthusiast and now co-host,
				Sarah, at a local gaming convention. They instantly hit it off, bonding over their mutual
				love for video games and their shared sense of humor. They quickly became inseparable gaming
				buddies, spending countless hours gaming together and cracking jokes that had them in
				stitches. It wasn't long before they realized that their gaming conversations and banter
				were too good to keep to themselves, and the idea of starting a podcast was born!
			</p>
			<p>
				Matt and Sarah poured their hearts and souls into creating the "Get Played" podcast. They
				spent hours researching and planning, and even more hours recording and editing their
				episodes. Their friendly and happy tone, peppered with Matt's signature bad jokes, became
				the hallmark of the podcast. They covered everything from the latest game releases to gaming
				news, reviews, and humorous anecdotes from their gaming experiences. Their chemistry and
				comedic timing were undeniable, and the podcast quickly gained a loyal following of avid
				gamers who couldn't get enough of their entertaining and informative content.
			</p>
			<p>
				Today, Matt Apodaca's life is a whirlwind of gaming adventures and podcast success. He's
				living his dream of combining his love for gaming with his comedic talents, and he's
				grateful every day for the opportunity to share his passion with others through the "Get
				Played" podcast. Matt and Sarah continue to create engaging and hilarious episodes, bringing
				joy and laughter to gamers all over the world. Their podcast has become a community for
				fellow gaming enthusiasts to connect, share stories, and laugh along with Matt's bad jokes.
				Matt's journey from a gaming-loving kid to a podcast host is a testament to the power of
				following your passion and letting your unique talents shine, and he's excited to see where
				the future takes him on this amazing gaming adventure!
			</p>
		</div>
		<div
			class="box flip"
			style:transform={`translate3d(33vw, ${scroll * -0.5}px, 0) rotate(${scroll * -0.7}deg)`}
		>
			<img src="../img/flip_roll.png" alt="" />
		</div>
		<div
			class="box flip"
			style:transform={`translate3d(53vw, ${scroll * -0.6}px, 0) rotate(${scroll * -0.8}deg)`}
		>
			<img src="../img/flip_roll.png" alt="" />
		</div>
		<div
			class="box flip"
			style:transform={`translate3d(13vw, ${scroll * -0.8}px, 0) rotate(${scroll * -1.1}deg)`}
		>
			<img src="../img/flip_roll.png" alt="" />
		</div>
	</section>
</body>

<!-- svelte-ignore css-unused-selector -->
<style lang="scss">
	@import '../src/lib/basecamp';
	body {
		margin-top: 4rem;
		scroll-behavior: smooth;
		transition: transform 0.2s ease-in-out;
		margin-bottom: 1px;
		overflow: hidden;
	}

	.box {
		height: fit-content;
		width: 100vw;
		background: $backMain;

		p {
			padding: $pad_xl $pad_sm;
		}
	}

	h1 {
		position: fixed;
		z-index: 420;
	}

	.main {
		margin-top: -3rem;
	}

	.flip {
		background-color: transparent;
		width: 100px;
		height: 100px;

		img {
			width: 100vw;
		}
	}

	@media (min-width: 1000px) {
		img {
			margin: 0 10vw;
		}
	}
</style>
