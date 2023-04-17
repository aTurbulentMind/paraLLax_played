<script>
	import Svg from '../../lib/insta.svelte';
	import Disco from '../../lib/disco.svelte';
</script>

<body>
	<h1>Join us:</h1>

	<div class="box">
		<a href="https://discord.gg/getplayed/"> <Disco /></a>
		<p>
			Discord: Lorem ipsum dolor sit amet consectetur adipisicing elit. Minus quisquam ut, dolor
			sapiente veniam odio iusto cum veritatis, tempore nihil incidunt doloremque alias atque nisi
			animi possimus deleniti asperiores nesciunt!
		</p>
		<a href="https://discord.gg/getplayed/">Join us</a>
	</div>
	<br /><br /><br />
	<div class="box">
		<a href="https://www.instagram.com/getplayedpod/"><Svg /> </a>
		<p>
			Instagram: Lorem ipsum dolor sit amet consectetur adipisicing elit. Doloremque reiciendis
			tenetur, modi voluptate quas laudantium distinctio nobis!
		</p>
		<a href="https://www.instagram.com/getplayedpod/">Follow us</a>
	</div>
</body>

<!-- svelte-ignore css-unused-selector -->
<style lang="scss">
	@import '../src/lib/basecamp';

	body {
		margin-top: 4rem;
	}

	.box {
		height: fit-content;

		a {
			margin: 10% 20%;
		}
	}

	@media (max-width: 768px) {
	}

	@media only screen and (min-width: 769px) {
	}

	@media only screen and (min-width: 1280px) {
	}
</style>
