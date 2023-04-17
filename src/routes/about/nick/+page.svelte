<script lang="ts">
	let scroll!: number;
	if (typeof window !== 'undefined') {
		scroll = window.scrollY;
		window.addEventListener('scroll', handleScroll);
	}

	function handleScroll() {
		scroll = window.pageYOffset;
		const vox1 = document.querySelector('.vox1');
		const vox2 = document.querySelector('.vox2');
		const vox3 = document.querySelector('.vox3');
		const vox4 = document.querySelector('.vox4');
		const vox5 = document.querySelector('.vox5');

		if (scroll > 350 && scroll < 824) {
			vox1.style.opacity = 1;
		} else {
			vox1.style.opacity = 0;
		}

		if (scroll > 450 && scroll < 950) {
			vox2.style.opacity = 1;
		} else {
			vox2.style.opacity = 0;
		}

		if (scroll > 650 && scroll < 1050) {
			vox3.style.opacity = 1;
		} else {
			vox3.style.opacity = 0;
		}

		if (scroll > 800 && scroll < 1200) {
			vox4.style.opacity = 1;
		} else {
			vox4.style.opacity = 0;
		}

		if (scroll > 1150 && scroll < 1550) {
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
			<img src="../img/nick.png" alt="" />
		</div>
		<div class="vox vox1" />
		<div class="vox vox2" />
		<div class="vox vox3" />
		<div class="vox vox4" />
		<div class="vox vox5" />
		<div class="box host">
			<p>
				I've always been the type of person who appreciates the finer things in life: a perfectly
				cooked steak, a well-crafted cup of coffee, and of course, video games. From the moment I
				got my first Game Boy, I was hooked. Gaming became my escape, my passion, my reason for
				living - or at least that's what I told my parents when they tried to pry me away from the
				console.
			</p>
			<p>
				As I grew older, my love for video games only intensified. I spent countless hours honing my
				skills, mastering every level, and defeating every boss. I became a connoisseur of gaming,
				with an encyclopedic knowledge of video game trivia and a sarcastic comment for every NPC
				dialogue.
			</p>
			<img src="../img/back.jpg" alt="" />
			<p>
				But it wasn't just about playing the games. I had opinions, strong opinions, about game
				mechanics, storylines, and character development. I couldn't resist sharing my dry and
				sarcastic commentary on gaming forums and social media, much to the chagrin of my
				less-enlightened friends who didn't quite get my sophisticated sense of humor.
			</p>
			<p>
				But it wasn't just about playing the games. I had opinions, strong opinions, about game
				mechanics, storylines, and character development. I couldn't resist sharing my dry and
				sarcastic commentary on gaming forums and social media, much to the chagrin of my
				less-enlightened friends who didn't quite get my sophisticated sense of humor.
			</p>
			<img src="../img/back.jpg" alt="" />
			<p>
				One day, as I was ranting about the lack of save points in a popular RPG on a gaming forum,
				I received a message from a fellow gamer who shared my sarcastic wit and passion for gaming.
				We instantly hit it off, and after hours of trading barbs and debating the merits of
				different gaming consoles, we realized we had something special.
			</p>
			<p>
				The Get Played podcast quickly gained a cult following among fellow gaming enthusiasts who
				appreciated our dry and sarcastic first-person tone. We dissected game mechanics with
				surgical precision, critiqued storylines with ruthless honesty, and roasted game developers
				for their questionable design choices. Our witty banter and unapologetic opinions struck a
				chord with gamers who were tired of generic gaming reviews and wanted something more
				authentic and entertaining.
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
		height: 60vh;
		width: 36vw;
		transition: opacity 0.1s ease-in-out;
		opacity: 0;
		margin-left: -2vw;

		h2 {
			font-size: $f-xxl;
		}
	}

	.vox1 {
		background-color: red;
		top: 16rem;
		left: 6vw;
	}

	.vox2 {
		background-color: green;
		top: 9rem;
		left: 2vw;
	}

	.vox3 {
		background-color: blue;
		top: 10rem;
		left: 20vw;
	}

	.vox4 {
		background-color: rgb(255, 0, 234);
		top: 16rem;
		left: 66vw;
	}
	.vox5 {
		background-color: rgb(255, 230, 0);
		top: 16rem;
		left: 66vw;
	}

	.host {
		height: fit-content;
	}

	.test {
		background: #fff;
	}
</style>
