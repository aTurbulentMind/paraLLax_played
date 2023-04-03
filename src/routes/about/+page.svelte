<script>
	let scroll;
	let speed = 2;
	let speed_2 = -2;
	let test = -0.5;
	let test_2 = 1;
</script>

<svelte:window bind:scrollY={scroll} />
<body>
	<h1>{scroll}</h1>
	<section>
		<div class="box test" style:transform={`translate3d( ${scroll}px, 0, 0)`} />
		<div class="box test" style:transform={`translate3d( ${scroll}px,0, 0)`} />
		<div class="box test" style:transform={`translate3d( ${scroll}px,0, 0)`} />
		<div class="box empty" />

		<div class="box l_b" style:transform={`translate3d(0, ${scroll * -1}px, 0)`} />
		<div class="box c_b" style:transform={`translate3d(15vw, ${scroll * -1}px, 0)`} />
		<div class="box r_b" style:transform={`translate3d(33vw, ${scroll * -1}px, 0)`} />
		<div class="box empty" />
		<div class="box empty" />
		<div class="box" />
		<div class="box" />
		<div class="box" />
		<div class="box test" style:transform={`translate3d(0, ${scroll * speed_2}px, 0)`} />
		<div class="box test" style:transform={`translate3d(0, ${scroll * speed_2}px, 0)`} />
		<div class="box" />
		<div class="box" />
		<div class="box test" style:transform={`translate3d(0, ${scroll * speed_2}px, 0)`} />
		<div class="box test" style:transform={`translate3d(0, ${scroll * speed_2}px, 0)`} />
	</section>

	<!--
		<div class="box pin" />
		<div class="box empty" />
		style:transform={`translate3d(0, ${scroll * -0.5}px, 0)`}
		style:transform={`translate3d(20px, ${scroll / 0.5}px, 0)`}
		style:transform={`translate3d(0, ${scroll * speed}px, 0)`}
		style:transform={`translate3d( ${scroll * test}px,0, 0)`}
		style:transform={`translate3d( ${scroll * test_2}px,${scroll * -2}px, 0)`}
		style:transform={`translate3d(66vw, ${scroll * -0.5}px, 0)`}
	-->
</body>

<!--svelte-ignore css-unused-selector -->
<style>
	body {
		margin-top: 4rem;
		scroll-behavior: smooth;

		background-image: url(img/back.jpg);
		background-repeat: no-repeat;
		background-attachment: fixed;
		background-position: center;
		background-size: 100%;
	}

	.box {
		--size: 300px;
		height: var(--size);
		width: 100vw;
		background: rgb(163, 87, 250);
		border: 1px solid black;
		margin-bottom: 1rem;
	}

	h1,
	.box {
		margin: 0 -8px;
	}
	h1 {
		position: fixed;
		z-index: 10;
	}

	.pin {
		position: fixed;
		margin-left: -8px;
		width: 105vw;
	}

	.empty {
		background: transparent;
	}

	.l_b {
		background: red;
		width: 66vw;
	}

	.c_b {
		background: chartreuse;
		width: 66vw;
	}

	.r_b {
		background: rgb(179, 109, 5);
		width: 66vw;
	}

	.test {
		background: rgb(0, 255, 255);
	}
</style>
