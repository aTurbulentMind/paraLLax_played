<script>
	let scroll;
	let speed = 2;
	let test = -0.5;
	let test_2 = 1;
</script>

<svelte:window bind:scrollY={scroll} />
<body>
	<h1>{scroll}</h1>
	<section>
		<!--<div class="box pin" />
		
		<div
			class="box"
			style:transform={`translate3d(0, ${scroll * speed}px, 0)`}
			style:background="teal"
		/>

		<div
			class="box"
			style:transform={`translate3d(20px, ${scroll / 0.5}px, 0)`}
			style:background="blue"
		/>
		<div
			class="box"
			style:transform={`translate3d( ${scroll * test}px,0, 0)`}
			style:background="purple"
		/>
		<div
			class="box"
			style:transform={`translate3d( ${scroll * test_2}px,${scroll * -2}px, 0)`}
			style:background="orange"
		/>

		<div
			class="box"
			style:transform={`translate3d(0, ${scroll * -0.5}px, 0)`}
			style:background="red"
		/>
	
	-->
		<div class="box" />
		<div class="box empty" />
		<div class="box" />
		<div class="box" />
		<div class="box" />
		<div class="box" />
		<div class="box empty" />
		<div class="box" />
		<div class="box" />
	</section>
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
</style>
