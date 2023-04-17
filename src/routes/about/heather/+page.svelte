<script lang="ts">
	let scroll!: number;

	let threshold1 = 400;
	let threshold2 = 550;
	let threshold3 = 750;
	let threshold4 = 750;
	let threshold5 = 1200;

	let threshold1_e = 924;
	let threshold2_e = 850;
	let threshold3_e = 1100;
	let threshold4_e = 1200;
	let threshold5_e = 1650;
	if (typeof window !== 'undefined') {
		scroll = window.scrollY;
		window.addEventListener('scroll', handleScroll);
	}

	// Update the opacity based on scroll value
	function handleScroll() {
		scroll = window.pageYOffset;
		const vox1 = document.querySelector('.vox1');
		const vox2 = document.querySelector('.vox2');
		const vox3 = document.querySelector('.vox3');
		const vox4 = document.querySelector('.vox4');
		const vox5 = document.querySelector('.vox5');

		if (scroll > threshold1 && scroll < threshold1_e) {
			vox1.style.opacity = 1;
		} else {
			vox1.style.opacity = 0;
		}

		if (scroll > threshold2 && scroll < threshold2_e) {
			vox2.style.opacity = 1;
		} else {
			vox2.style.opacity = 0;
		}

		if (scroll > threshold3 && scroll < threshold3_e) {
			vox3.style.opacity = 1;
		} else {
			vox3.style.opacity = 0;
		}

		if (scroll > threshold4 && scroll < threshold4_e) {
			vox4.style.opacity = 1;
		} else {
			vox4.style.opacity = 0;
		}

		if (scroll > threshold5 && scroll < threshold5_e) {
			vox5.style.opacity = 1;
		} else {
			vox5.style.opacity = 0;
		}
	}
</script>

<svelte:window bind:scrollY={scroll} />
<body>
	<section>
		<div class="box">
			<img src="../img/heather.jpg" alt="" />
		</div>
		<div class="vox vox1">
			<img src="../img/pew.png" alt="" />
		</div>
		<div class="vox vox2">
			<img src="../img/pew_pew.png" alt="" />
		</div>
		<div class="vox vox3">
			<img src="../img/pew_pew_pew.png" alt="" />
		</div>
		<div class="vox vox4">
			<img src="../img/pew.png" alt="" />
		</div>
		<div class="vox vox5">
			<img src="../img/pewpew.png" alt="" />
		</div>
		<div class="box host">
			<p>
				Heather Anne Campbell, a passionate gamer with an unwavering love for combat, has had quite
				the adventurous journey that ultimately led her to co-hosting the wildly popular Get Played
				podcast. Growing up, Heather was always captivated by video games, and she spent countless
				hours honing her skills and achieving impressive kill counts in various games.
			</p>
			<p>
				As a young gamer, Heather explored a wide array of gaming genres, but she always found
				herself gravitating towards games that involved intense combat. She thrived in fast-paced,
				action-packed games, and she became known among her friends for her sharp reflexes and
				strategic gameplay. She was the go-to person in her gaming circle for tips on how to get all
				of the kills and dominate the competition.
			</p>
			<img src="../img/back.jpg" alt="" />
			<p>
				Heather's passion for gaming continued to flourish as she grew older, and she spent
				countless late nights honing her skills and competing in online multiplayer games. She
				became known in the gaming community for her prowess in games like Fortnite, where her love
				for combat and her dedication to achieving high kill counts truly shone. Her exceptional
				gameplay and competitive spirit earned her recognition and respect among her fellow gamers.
			</p>
			<p>
				Heather's gaming journey eventually led her to co-hosting the Get Played podcast, where she
				could share her love for gaming with a wider audience. She brought her infectious
				enthusiasm, sharp insights, and a friendly, happy tone to the podcast, as she shared her
				experiences, strategies, and tips for gaming success. Her deep knowledge of combat-oriented
				games like Fortnite and her passion for achieving high kill counts made her a valuable asset
				to the podcast, and she quickly became a fan favorite among listeners.
			</p>
			<img src="../img/back.jpg" alt="" />
			<p>
				Heather's love for gaming, particularly her affinity for combat and achieving high kill
				counts, has been a driving force in her life and has ultimately led her to where she is
				today - co-hosting a successful gaming podcast and sharing her passion with fellow gamers
				around the world. Her dedication, skill, and friendly personality continue to make her a
				beloved figure in the gaming community, and she continues to inspire and entertain gamers
				with her enthusiasm for all things gaming, especially Fortnite and other combat-oriented
				games.
			</p>
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
	}

	.box {
		height: fit-content;
		width: 100vw;
		background: $backMain;
		padding: $pad;
		h1 {
			position: fixed;
			margin-top: 20vh;
			font-size: $f-xxl;
		}

		a {
			color: $textMain;
		}
	}

	.vox {
		position: fixed;
		height: fit-content;
		transition: opacity 0.1s ease-in-out;
		opacity: 0;
		margin-left: -2vw;

		h2 {
			font-size: $f-xxl;
		}

		img {
			height: 25vh;
		}
	}

	.vox1 {
		height: 25vh;
		bottom: 2rem;
		left: 6vw;
	}

	.vox2 {
		top: 19rem;
		left: 40vw;
	}

	.vox3 {
		top: 15rem;
		left: 70vw;
	}

	.vox4 {
		height: 25vh;
		bottom: 2rem;
		left: 6vw;
	}
	.vox5 {
		height: 35vh;
		bottom: 2rem;
		left: 6vw;
	}

	.host {
		height: fit-content;
	}

	@media (min-width: 1000px) {
		img {
			margin: 0 10vw;
		}
	}
</style>
