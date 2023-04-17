<script lang="ts">
	let scroll!: number;
	if (typeof window !== 'undefined') {
		scroll = window.scrollY;
	}
</script>

<svelte:window bind:scrollY={scroll} />
<body>
	<!--	<h1>{scroll}</h1>-->
	<section>
		<div class="box">
			<p>
				Lorem ipsum dolor sit amet consectetur adipisicing elit. Obcaecati rem tempore magnam eaque
				ipsa voluptatibus! Esse ducimus tempore unde iure officiis, animi in? Consequuntur deserunt,
				hic distinctio ducimus quo facere?
			</p>
		</div>
		<div class="box">
			<p>
				Lorem ipsum dolor sit amet consectetur adipisicing elit. Obcaecati rem tempore magnam eaque
				ipsa voluptatibus! Esse ducimus tempore unde iure officiis, animi in? Consequuntur deserunt,
				hic distinctio ducimus quo facere?
			</p>
		</div>
		<div style:--scroll="{scroll}px" class="box bott_box">
			<p>
				Lorem ipsum dolor sit amet consectetur adipisicing elit. Obcaecati rem tempore magnam eaque
				ipsa voluptatibus! Esse ducimus tempore unde iure officiis, animi in? Consequuntur deserunt,
				hic distinctio ducimus quo facere?
			</p>
		</div>
	</section>
</body>

<!-- svelte-ignore css-unused-selector -->
<style lang="scss">
	@import '../src/lib/basecamp';
	:root {
		--yellow: #cecb1;
	}

	body {
		margin-top: 4rem;
		scroll-behavior: smooth;
		transition: transform 0.2s ease-in-out;
	}

	.box {
		height: 100vh;
		width: 105vw;
		background: $highlight;
	}

	.bott_box {
		background-color: $grabber;
		z-index: 999;
		height: fit-content;
		transform: translate3d(0, calc(var(--scroll) * -0.35), 0);

		@media only screen and (min-width: 768px) {
			transform: translate3d(0, calc(var(--scroll) * -0.5), 0);
		}
	}

	@media only screen and (min-width: 768px) {
	}
</style>
