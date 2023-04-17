<script lang="ts">
	import Disco from '../lib/disco.svelte';
	import Svg from '../lib/insta.svelte';

	let scroll!: number;
	if (typeof window !== 'undefined') {
		scroll = window.scrollY;
		window.addEventListener('scroll', handleScroll);
	}

	let angle = 0;

	let hue = 110;

	let minOpacity = 0;
	let maxOpacity = 1;
	let minScroll = 0;
	let maxScroll = 1000;

	$: angle = (scroll / 1000) * 360;
	$: hue = scroll / 10;

	function getOpacity(scroll: number) {
		let value = (scroll - minScroll) / (maxScroll - minScroll);
		return Math.min(Math.max(value, minOpacity), maxOpacity);
	}

	function handleScroll() {
		scroll = window.pageYOffset;
		const vox1 = document.querySelector('.vox1');
		const vox2 = document.querySelector('.vox2');
		const vox3 = document.querySelector('.vox3');
		const vox4 = document.querySelector('.vox4');
		const vox5 = document.querySelector('.vox5');

		if (scroll > 50 && scroll < 850) {
			vox1.style.opacity = 1;
		} else {
			vox1.style.opacity = 0;
		}

		if (scroll > 150 && scroll < 850) {
			vox2.style.opacity = 1;
		} else {
			vox2.style.opacity = 0;
		}

		if (scroll > 350 && scroll < 850) {
			vox3.style.opacity = 1;
		} else {
			vox3.style.opacity = 0;
		}

		if (scroll > 550 && scroll < 850) {
			vox4.style.opacity = 1;
		} else {
			vox4.style.opacity = 0;
		}

		if (scroll > 100 && scroll < 850) {
			vox5.style.opacity = 1;
		} else {
			vox5.style.opacity = 0;
		}
	}
</script>

<svelte:window bind:scrollY={scroll} />
<body>
	<!--	<h1>{scroll}</h1>-->
	<section>
		<div class="vox vox5" />
		<div
			class="box hue ent"
			style:transform={`translate3d(${scroll > 100 ? (scroll - 100) * 1 : 0}px, 0, 0)`}
			style:background={`hsl(${hue + scroll}, 42%, 22%)`}
			style:filter={`blur(${scroll / 10}px)`}
		>
			<h1>Welcome to the worlds premier video game podcast! With your hosts:</h1>
		</div>

		<div class="vox vox1">
			<img src="img/h_ent2.png" alt="" />
			<p>Heather <br /> Anne <br /> Campbell</p>
		</div>
		<div class="vox vox2">
			<img src="img/m_ent2.png" alt="" />
			<p>Matt <br />Apidoca</p>
		</div>
		<div class="vox vox3">
			<img src="img/n_ent2.png" alt="" />
			<p>Nick <br />Wiger</p>
		</div>
		<div class="vox vox4"><h2>And this is</h2></div>

		<div class="box host">
			<p>
				Are you ready to level up your video game knowledge? Welcome to the Get Played Podcast, the
				show where we talk about all things gaming. Whether you're a casual player or a die-hard
				fan, our expert hosts are here to guide you through the world of gaming with humor, insight,
				and plenty of puns. So grab your controller and let's dive into the world of gaming!
			</p>
			<p>
				Do you love video games? Are you looking for a fun, lighthearted podcast to listen to while
				you play? Then you're in the right place! The Get Played Podcast is your go-to source for
				all things gaming. From the latest releases to classic favorites, our hosts have got you
				covered. Plus, we'll throw in some hilarious gaming jokes and puns to keep you entertained
				along the way.
			</p>

			<img src="img/otho.jpg" alt="" />
		</div>
		<div class="box l_b" style:--scroll="{scroll}px">
			<a href="/"><Disco /> </a>
		</div>
		<div class="box c_b" style:--scroll="{scroll}px">
			<a href="/"><Disco /> </a>
		</div>
		<div class="box r_b" style:--scroll="{scroll}px">
			<a href="/"> <Svg /></a>
		</div>
		<div class="box bott_box" style:--scroll="{scroll}px">
			<p>
				Welcome to the Get Played Podcast, where gaming meets comedy. Our hosts are experts in all
				things gaming, but they're also hilarious comedians. Join us each week as we discuss the
				latest video game news, share our favorite gaming moments, and make you laugh with our
				gaming puns and jokes. It's like playing video games with your funniest friends!
			</p>
			<img src="img/back.jpg" alt="" />
			<p>
				Do you remember the good old days of gaming, when all you needed was a joystick and a
				button? Well, those days may be gone, but the fun of gaming lives on with the Get Played
				Podcast. Our hosts are passionate about all things gaming, from retro classics to modern
				hits. And with our gaming jokes and puns, you'll be laughing your way through the world of
				gaming. So put on your gaming headset and let's get started!
			</p>
		</div>
	</section>
</body>

<!-- svelte-ignore css-unused-selector -->
<style lang="scss">
	@import '../src/lib/basecamp';


.my-element {
  background-color: var(--primary-color);
  height: 100vh;
}
	body {
		--scroll:${scroll};
		margin-top: 4rem;
		scroll-behavior: smooth;
		transition: transform 0.2s ease-in-out;
		background-image: url(img/back.jpg);
		background-repeat: no-repeat;
		background-attachment: fixed;
		background-position: center;
		background-size: 100%;
	}

	.box {
		height: fit-content;
		width: 105vw;
		background: $backMain;
		margin: 0 -8px 1rem -8px;
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

	.dox {
		height: 100vh;
		width: 105vw;
		background: $highlight;
		margin: 0 -8px 1rem -8px;
		padding: $pad;
		
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
		top: 8rem;
	}

	.vox2 {
		top: 9rem;
		left: 33vw;
	}

	.vox3 {
		top: 10rem;
		left: 66vw;
	}

	.vox4 {
		background-color: $highlight;
		height: fit-content;
		top: 25rem;
		left: 0;
		width: 100vw;
		margin: -5vh 0;

		h2 {
			margin: 5vh 20vw;
		}
	}

	.vox5 {
		background-color: $backMain;
		height: 100vh;
		top: 0;
		left: 0;
		width: 100vw;
	}

	.ent {
		height: 225vh;
	}

	.hue {
		transition: background-color 0.2s ease-in-out;
	}

	.host {
		height: fit-content;
	}

	.test {
		background: #fff;
	}

	.bott_box {
		background-color: $backMain;
		height: fit-content;
		transform: translate3d(0, calc(var(--scroll) * -0.35), 0);

		@media only screen and (min-width: 768px) {
			transform: translate3d(0, calc(var(--scroll) * -0.2), 0);
		}
		@media only screen and (min-width: 1280px) {
			transform: translate3d(0, calc(var(--scroll) * -0.25), 0);
		}
	}

	.l_b {
		background: red;
		width: 33vw;
		transform: translate3d(0, calc(var(--scroll) * 0.15), 0);

		@media only screen and (min-width: 768px) {
			transform: translate3d(0, calc(var(--scroll) * 0.35), 0);
		}
	}

	.r_b {
		background: rgb(179, 109, 5);
		width: 33vw;
		transform: translate3d(66vw, calc(var(--scroll) * 0.15), 0);

		@media only screen and (min-width: 768px) {
			transform: translate3d(66vw, calc(var(--scroll) * 0.25), 0);
		}
	}

	.c_b {
		background: chartreuse;
		width: 33vw;
				transform: translate3d(33vw, calc(var(--scroll) * 0.22), 0);

		@media only screen and (min-width: 768px) {
			transform: translate3d(33vw, calc(var(--scroll) * 0.35), 0);
		}
	}

	.blur-effect {
		display: flex;
		flex-direction: column;
		align-items: center;
		justify-content: center;
		height: 100vh;
		width: 100%;
		background-color: #f6f6f6;
		transition: filter 0.2s;
	}

	.empty {
		background: transparent;
	}

	@media only screen and (min-width: 768px) {
		.host,
		.bott_box {
			img {
				width: 80vw;
				height: 70vh;
				margin: 0 10vw;
			}
		}

		img {
			height: 50vh;
		}

		
	.vox4 {
		height: fit-content;
		padding: 12vh 7vw;
	}
	}
</style>
