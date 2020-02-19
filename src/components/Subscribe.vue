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
#subscribe {
	width: 100%;
	padding: 2rem;
	background: #0E0B16;
	color: #E7DFDD;

	h2 { padding-bottom: 2rem; }
	a { color: #E7DFDD; }
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
			transition: background-color .1s cubic-bezier(.52,.41,.81,.09);

			a,
			p { transition: color .1s cubic-bezier(.52,.41,.81,.09); }
			&:hover {
				background: #E7DFDD;

				a,
				p { color: #0E0B16; }
			}
			a {
				font-size: 32px;
				color: #E7DFDD;
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
			background: #E7DFDD;
		}
	}
}
</style>
