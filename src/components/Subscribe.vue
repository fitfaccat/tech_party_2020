<template>
	<section id="subscribe">
		<h2>Agora te inscreve aí tchê...</h2>

		<section>
			<article>
				<a href="#">QUERO ME INSCREVER</a>
			</article>
			<div class="line">

			</div>
			<article>
				<img src="https://cdljoinville.jv200.net/wp-content/uploads/sites/189/2018/02/%C3%8Dcone-Certificado-Digital.png" alt="Certificado">
				<p>
					Neste sentido, a constante divulgação das informações desafia a capacidade de equalização do levantamento das variáveis envolvidas.
				</p>
			</article>
		</section>

	</section>
</template>

<script>
export default {
  name: 'Subscribe'
}
</script>

<style scoped lang="scss">
@import './../assets/sass/variables.scss';

#subscribe {
	width: 100%;
	padding: 2rem;
	background: $primary-color;
	color: $secundary-color;

	h2 { padding-bottom: 2rem; }
	a { color: $secundary-color; }
	section {
		display: flex;

		article {
			flex: 1;
			padding: 2rem;
			display: flex;
			flex-direction: column;
			align-items: center;
			justify-content: center;
			cursor: pointer;
			transition:
          background-color
          $transition-duration
          $transition-timing-function;

			a,
			p {
				transition:
          color
          $transition-duration
          $transition-timing-function;
			}
			&:hover {
				background: $secundary-color;

				a,
				p { color: $primary-color; }
			}
			a {
				font-size: 32px;
				color: $secundary-color;
				font-weight: bold;
			}
			img { width: 85%; }
			p {
				padding: 0 2rem;
				text-align: justify;
			}
		}
		.line {
			width: .25rem;
			background: $secundary-color;
		}
	}
}
</style>
