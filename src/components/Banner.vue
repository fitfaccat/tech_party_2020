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
@import './../assets/sass/variables.scss';

#banner {
	position: relative;
	width: 100%;
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
		color: $secundary-color;
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
			border: 2px solid $secundary-color;
			padding: 1rem 2rem;
			color: $secundary-color;
			font-weight: bold;
			border-radius: 1rem;
			transition:
				background-color
				$transition-duration
				$transition-timing-function;
			transition:
				color
				$transition-duration
				$transition-timing-function;

			&:hover {
				color: $primary-color;
				background: $secundary-color;
			}
		}
	}
}
</style>