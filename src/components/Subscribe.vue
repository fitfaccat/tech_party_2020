<template>
	<section id="subscribe" class="fullhd-font-size">
		<h2>Agora te inscreve aí tchê...</h2>
		<section>
			<article>
				<a href="https://saga2.faccat.br/index.php?op=1068&chave=1739&portal=E" target="_blank">QUERO ME INSCREVER</a>
			</article>
			<div class="line"></div>
			<article>
				<img src="https://cdljoinville.jv200.net/wp-content/uploads/sites/189/2018/02/%C3%8Dcone-Certificado-Digital.png" alt="Certificado">
				<p>
					Após alguns dias do término do evento, cada participante inscrito e com presença confirmada (assinatura na lista de presença), receberá um e-mail com um link onde poderá fazer o download do seu Certificado de Participação!
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

		p { padding: 0 2rem; }

		article {
			flex: 1;
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
				width: 100%;
				height: 100%;
				display: flex;
				align-items: center;
				justify-content: center;
				font-size: 32px;
				font-weight: bold;
				color: $secundary-color;
			}
			img { width: 75%; }
			p {
				padding-bottom: 2rem;
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
