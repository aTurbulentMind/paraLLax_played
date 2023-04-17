<!---->
<script>
	let isMenuOpen = false;

	function toggleMenu() {
		isMenuOpen = !isMenuOpen;
	}

	let current = 0;
</script>

<div class="navbar">
	<a href="/" class="logo"><h1>GET PLAYED</h1></a>
	<nav class:open={isMenuOpen}>
		<!--this is the main navigation menu-->
		<ul>
			<li on:click={() => (isMenuOpen = false)} on:keydown={() => (isMenuOpen = false)}>
				<p>New episodes Monday</p>
			</li>

			<li on:click={() => (isMenuOpen = false)} on:keydown={() => (isMenuOpen = false)}>
				<a class:current={current === 0} on:click={() => (current = 0)} href="/">Home</a>
			</li>
			<li
				on:click={() => (isMenuOpen = false)}
				on:keydown={() => (isMenuOpen = false)}
				class="space"
			>
				<a
					class:current={current === 4}
					on:click={() => (current = 4)}
					href="https://www.earwolf.com/show_archive/get-played/">Podcast</a
				>
			</li>
			<li on:click={() => (isMenuOpen = false)} on:keydown={() => (isMenuOpen = false)}>
				<a
					class:current={current === 1}
					on:click={() => (current = 1)}
					href="https://www.podswag.com/collections/how-did-this-get-played/">Store</a
				>
			</li>
			<li on:click={() => (isMenuOpen = false)} on:keydown={() => (isMenuOpen = false)}>
				<a class:current={current === 2} on:click={() => (current = 2)} href="/contact">Follow</a>
			</li>
			<li
				on:click={() => (isMenuOpen = false)}
				on:keydown={() => (isMenuOpen = false)}
				class="space"
			>
				<a class:current={current === 3} on:click={() => (current = 3)} href="/about">About</a>
			</li>
		</ul>
	</nav>
	<button class="burger" on:click={toggleMenu}>
		<img src="/img/logo.jpg" alt="" />
	</button>
</div>

<!-- svelte-ignore css-unused-selector -->
<style lang="scss">
	@import 'basecamp';

	:global(*) {
		box-sizing: border-box;
	}

	.navbar {
		background-color: $textTwo;
		width: 100%;
		display: flex;
		justify-content: space-between;
		align-items: center;
		position: fixed;
		height: 4rem;
		z-index: 990;

		a {
			text-shadow: $text_shadow;
		}
	}

	.logo {
		margin-left: 4vw;

		h1 {
			font-size: $font;
		}
	}

	@media only screen and (max-width: 767px) {
		nav {
			display: none;
		}

		nav.open {
			display: block;
			position: absolute;
			top: 100%;
			left: 0;
			background-color: $backTwo;
			width: 100%;
		}
	}

	ul {
		display: flex;
		flex-direction: column;
		justify-content: space-between;
		align-items: center;
		gap: 5vh;
		margin-top: 2vh;
		margin-bottom: 4vh;
		list-style: none;
		font-size: $f-sm;

		li {
			p {
				margin-top: 1vh;
				margin-bottom: 1vh;
				font-size: $f-sm;
				color: $highlight;
				text-shadow: $text_shadow;
			}
		}
	}

	.current {
		position: relative;
	}

	.current::after {
		content: '';
		position: absolute;
		bottom: 0;
		left: 0;
		width: 100%;
		height: 2px;
		background-color: $extra;
	}

	.burger {
		height: 46px;
		aspect-ratio: 1;
		background-color: transparent;

		margin-right: 6vw;
		display: flex;
		align-items: center;
		justify-content: center;

		&:hover {
			cursor: pointer;
		}
	}
	.burger > div {
		height: 2px;
		width: 14px;
		background-color: $highlight;
		position: absolute;
	}

	@media only screen and (min-width: 768px) {
		.logo {
			margin-left: 3vw;
		}

		.burger {
			display: none;
		}

		nav {
			display: block;
			position: relative;
			height: 4rem;
		}

		.navbar {
			height: 5rem;
		}

		.logo {
			margin-left: 1vw;
		}

		ul {
			margin: 0;
			flex-direction: row;
			gap: 2vw;
		}

		.space {
			margin-right: 2vw;
		}
	}
</style>
