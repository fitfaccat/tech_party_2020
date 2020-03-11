<template>
	<section id="churras" class="fullhd-font-size">
		
		<h2>O melhor churras do mundo!</h2>

		<section>
			<article>
				<img src="https://techparty.faccat.br/2018/img/qr-2018.png" alt="QRcode Churras">
			</article>
			<article>
				<div class="wrap-text">
					<p>Lorem, ipsum dolor sit amet consectetur adipisicing elit. Architecto, adipisci dicta rerum ex inventore sed quam veniam repellendus ipsam molestiae alias placeat sapiente. Doloribus veritatis dignissimos architecto, vel neque modi.</p>
					<p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Quia deleniti nulla at ea delectus ad quos ex laudantium recusandae modi, perferendis expedita ullam laborum reiciendis neque hic voluptate repellendus nesciunt.</p>
					<p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Quod, nemo! Fugit voluptatum quis temporibus quo odio praesentium. Illum mollitia ducimus inventore quasi in assumenda alias? Fuga facilis odit culpa quam?</p>
				</div>
			</article>
		</section>

	</section>
</template>

<script>
export default {
  name: 'Churras'
}
</script>

<style scoped lang="scss">
@import './../assets/sass/variables.scss';

#churras {
	width: 100%;
	padding: 2rem;
	color: $secundary-color;

	h2 { padding-bottom: 2rem; }
	section {
		display: flex;
		
		article {
			flex: 1;
			display: flex;
			flex-direction: column;
			align-items: center;
			justify-content: space-around;
		}
		article {
			border: 1px solid $primary-color;

			img { width: 75%; }
			.wrap-text {
				padding: 2rem;
				
				p {
					padding: 1rem;
					text-align: justify;
				}
			}
		}
	}
}

/* responsive */
@media (max-width: 850px) {
	#churras section article .wrap-text {
		padding: 2rem 0;
	}
}
@media (max-width: 600px) {
	#churras {
		padding: 0;

		h2 {
			padding: 2rem;
			font-size: 20px;
		}
		section { flex-direction: column; }
	}
}
</style>
