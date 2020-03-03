<template>
	<section id="banner">
		<div class="filter"></div>
		<article>
			<img src="https://techparty.faccat.br/images/logos/techparty-logo.png" alt="">
			<div>27 a 30 de Abril - FACCAT</div>
			<Countdown
				dateEvent="1588015800000"
			/>
			<a href="https://saga2.faccat.br/index.php?op=1068&chave=1739&portal=E" target="_blank">INSCREVA-SE</a>
		</article>
	</section>
</template>

<script>
import Countdown from './countdown/Countdown.vue';

export default {
	name: 'Banner',
	components: {
		Countdown
	}
}
</script>

<style scoped lang="scss">
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
		background: #000000a3;
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