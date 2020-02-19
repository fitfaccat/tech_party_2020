<template>
	<section id="local">

		<h2>E segue o rumo do teu próprio coração</h2>

		<section>
			<article id="address">
				<p>FACCAT</p>
				<p>Avenida Oscar Martins Rangel, 4500</p>
				<p>Bairro Fogão Gaúcho</p>
				<p>Taquara, Rio Grande do Sul</p>
			</article>
			<article id="maps">

			</article>
			<footer>
				<section>FOOTER 1</section>
				<section>FOOTER 2</section>
				<section>FOOTER 3</section>
			</footer>
		</section>

	</section>
</template>

<script>
export default {
  name: 'Local'
}
</script>

<style scoped lang="scss">
#local {
	width: 100%;
	padding: 2rem;
	background: #0E0B16;
	color: #E7DFDD;

	h2 {
		padding-bottom: 2rem;
	}
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
		footer {
			height: 50vh;
			flex-direction: row;
			justify-content: space-around;
		}
	}
}
</style>
