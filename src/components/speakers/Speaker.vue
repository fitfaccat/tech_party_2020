<template>
	<section :id="id">
		<article class="perfil-photo" v-if="evenMod === 0">
			<img :src="image" :alt="name">
		</article>
		<article class="perfil-info">
			<div class="perfil-wrap">
				<h2>{{ name }}</h2>
				<div class="social-links-content">
					<a href="#" class="social-links-items">
						<img src="../../assets/facebook-2020.png" alt="Facebook">
					</a>
					<a href="#" class="social-links-items">
						<img src="../../assets/linkedin-2020.png" alt="linkedin-2020">
					</a>
					<a href="#" class="social-links-items">
						<img src="../../assets/twiiter-2020.png" alt="Twiiter">
					</a>
				</div>
			</div>
			<p>
				Lorem ipsum, dolor sit amet consectetur adipisicing elit. Atque consequatur velit placeat dignissimos beatae quae modi alias doloremque architecto vel.
			</p>
		</article>
		<article class="perfil-photo" v-if="evenMod !== 0">
			<img :src="image" :alt="name">
		</article>
	</section>
</template>

<script>
export default {
  name: 'Speaker',
	props: {
		index:	Number,
		name: 	String,
		id:			String,
		image:	String
	},
	computed: {
		evenMod() {
			if (window.innerWidth > 600) {
				return this.index % 2;
			}
			return 0;
		}
	}
}
</script>

<style scoped lang="scss">
@import './../../assets/sass/variables.scss';

section {
	display: flex;

	h2 {
		padding-bottom: 0;
		color: $primary-color;
		padding: .5rem;
	}
	article {
		flex: 1;
		height: 300px;
		display: flex;
		align-items: center;
		justify-content: center;
	}
	.perfil-photo {
		background: $tertiary-color;

		img {
			height: 280px;
			width: 280px;
			border-radius: 50%;
			display: block;
		}
	}
	.perfil-info {
		display: flex;
		flex-direction: column;
		background: $secundary-color;

		p,
		.perfil-wrap { flex: 1 }
		.perfil-wrap {
			width: 100%;
			display: flex;
			align-items: center;
			justify-content: space-around;
			
			.social-links-content {
				display: flex;
				align-items: center;
				justify-content: center;

				.social-links-items {
					img {
						padding: .5rem;
						display: block;
						width: 48px;
						
						&:hover { opacity: .8; }
					}
				}
			}
		}
		p {
			padding: 1rem 2rem;
			text-align: justify;
		}
	}
}

/* responsive */
@media (max-width: 650px) {
	section .perfil-photo img {
		max-width: 75%;
		height: initial;
	}
}
@media (max-width: 600px) {
	section {
		flex-direction: column;

		.perfil-info {
			.perfil-wrap {
				padding: 0 .5rem;
				
				.social-links-content {
					.social-links-items {
						img { padding: .3rem; }
					}
				}
			}
			p {
				padding: 1rem;
				flex: 2;
			}
		}
	}
}
</style>
