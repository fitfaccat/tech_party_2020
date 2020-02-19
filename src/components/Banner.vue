<template>
	<section id="banner">
		<div class="filter"></div>
		<article>
			<img src="https://techparty.faccat.br/images/logos/techparty-logo.png" alt="">
			<div>27 a 30 de Abril - FACCAT</div>
			<div id="timer">00:00:00:000</div>
			<a href="#">INSCREVA-SE</a>
		</article>
	</section>
</template>

<script>
export default {
  name: 'Banner'
}
</script>

<style scoped lang="scss">
@import url('https://fonts.googleapis.com/css?family=Roboto+Mono:700&display=swap');

#banner {
	position: relative;
	width: 100vw;
	height: 100vh;
	background: url('https://techparty.faccat.br/2018/img/banner-1.jpg') no-repeat center center fixed;
	background-size: cover;

	article,
	.filter {
		position: absolute;
		width: 100%;
		height: 100%;
	}
	.filter {
		backdrop-filter: blur(2px);
		background: #00000077;
	}
	article {
		display: flex;
		justify-content: center;
		align-items: center;
		flex-direction: column;
		color: white;
		font-size: 24px;

		img,
		div,
		a { margin: .5rem; }
		#timer {
			font-size: 42px;
			margin: 1rem;
			font-family: 'Roboto Mono', monospace;
		}
		a {
			border: 2px solid white;
			padding: 1rem 2rem;
			color: white;
			font-weight: bold;
			border-radius: 1rem;
			transition: background-color .1s cubic-bezier(.52,.41,.81,.09);
			transition: color .1s cubic-bezier(.52,.41,.81,.09);

			&:hover {
				color: black;
				background: white;
			}
		}
	}
}

</style>
