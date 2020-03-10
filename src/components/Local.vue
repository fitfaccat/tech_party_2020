<template>
	<section id="local" class="fullhd-font-size">
		<h2>E segue o rumo do teu próprio coração</h2>
		<section>
			<article id="address">
				<p>FACCAT</p>
				<p>Avenida Oscar Martins Rangel, 4500</p>
				<p>Bairro Fogão Gaúcho</p>
				<p>Taquara, Rio Grande do Sul</p>
			</article>
			<article id="maps"></article>
		</section>
	</section>
</template>

<script>
export default {
  name: 'Local'
}
</script>

<style scoped lang="scss">
@import './../assets/sass/variables.scss';

#local {
	width: 100%;
	padding: 2rem;
	background: $primary-color;
	color: $secundary-color;

	h2 { padding-bottom: 2rem; }
	section {
		article,
		footer {
			display: flex;
			flex-direction: column;
			align-items: center;
			justify-content: center;
		}
		#address {
			height: 50vh;
			font-size: 18px;

			p { padding: .25rem; }
		}
		#maps { height: 100vh; background: darkseagreen; }
	}
}
</style>
