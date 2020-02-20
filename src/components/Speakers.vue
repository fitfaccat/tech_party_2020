<template>
	<section id="speakers">
		<h2>Palestrantes...</h2>

		<section>
			<article class="perfil-photo">
				<img src="https://pbs.twimg.com/profile_images/988775660163252226/XpgonN0X_400x400.jpg" alt="Bill Gates">
			</article>
			<article class="perfil-info">
				<div class="perfil-wrap">
					<h3>Bill Gates</h3>
					<div class="social-links-content">
						<a href="#" class="social-links-items">
							<img src="https://logodownload.org/wp-content/uploads/2014/09/facebook-logo-2-1.png" alt="Facebook">
						</a>
						<a href="#" class="social-links-items">
							<img src="https://image.flaticon.com/icons/png/512/49/49656.png" alt="LinkedIn">
						</a>
						<a href="#" class="social-links-items">
							<img src="https://logodownload.org/wp-content/uploads/2014/09/twitter-logo-1-1.png" alt="Twiiter">
						</a>
					</div>
				</div>
				<p>
					Lorem ipsum, dolor sit amet consectetur adipisicing elit. Atque consequatur velit placeat dignissimos beatae quae modi alias doloremque architecto vel.
				</p>
			</article>
		</section>

		<section>
			<article class="perfil-info">
				<div class="perfil-wrap">
					<h3>Fausto Silva</h3>
					<div class="social-links-content">
						<a href="#" class="social-links-items">
							<img src="https://logodownload.org/wp-content/uploads/2014/09/facebook-logo-2-1.png" alt="Facebook">
						</a>
						<a href="#" class="social-links-items">
							<img src="https://image.flaticon.com/icons/png/512/49/49656.png" alt="LinkedIn">
						</a>
						<a href="#" class="social-links-items">
							<img src="https://logodownload.org/wp-content/uploads/2014/09/twitter-logo-1-1.png" alt="Twiiter">
						</a>
					</div>
				</div>
				<p>
					Lorem ipsum, dolor sit amet consectetur adipisicing elit. Atque consequatur velit placeat dignissimos beatae quae modi alias doloremque architecto vel.
				</p>
			</article>
			<article class="perfil-photo">
				<img src="https://www.flamengorj.com.br/arquivos/noticia/c3e65b0d-201d-47b7-aaab-af24cf7a6d87_quadrada.jpeg" alt="Fausto Silva">
			</article>
		</section>

		<section>
			<article class="perfil-photo">
				<img src="https://pm1.narvii.com/6447/142e2397fbb5e650b72d051bf8279c247b2273a7_00.jpg" alt="Chuck Norris">
			</article>
			<article class="perfil-info">
				<div class="perfil-wrap">
					<h3>Chuck Norris</h3>
					<div class="social-links-content">
						<a href="#" class="social-links-items">
							<img src="https://logodownload.org/wp-content/uploads/2014/09/facebook-logo-2-1.png" alt="Facebook">
						</a>
						<a href="#" class="social-links-items">
							<img src="https://image.flaticon.com/icons/png/512/49/49656.png" alt="LinkedIn">
						</a>
						<a href="#" class="social-links-items">
							<img src="https://logodownload.org/wp-content/uploads/2014/09/twitter-logo-1-1.png" alt="Twiiter">
						</a>
					</div>
				</div>
				<p>
					Lorem ipsum, dolor sit amet consectetur adipisicing elit. Atque consequatur velit placeat dignissimos beatae quae modi alias doloremque architecto vel.
				</p>
			</article>
		</section>

	</section>
</template>

<script>
export default {
  name: 'Speakers'
}
</script>

<style scoped lang="scss">
#speakers {
	width: 100%;
	padding: 2rem;
	background: #0E0B16;

	h2 {
		padding-bottom: 2rem;
		color: #E7DFDD;
	}
	section {
		// padding: 0 2rem;
		display: flex;

		article {
			flex: 1;
			height: 300px;
			display: flex;
			align-items: center;
			justify-content: center;
		}

		.perfil-photo {
			background: #E84C3D;

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
			background: #E7DFDD;

			p,
			.perfil-wrap { flex: 1 }
			.perfil-wrap {
				width: 100%;
				display: flex;
				align-items: center;
				justify-content: space-around;
			
				.social-links-content {
					display: flex;

					.social-links-items {
						img {
							padding: .5rem;
							display: block;
							width: 32px;
							height: 32px;
						}
					}
				}
			}

			p {
				padding: 1rem;
				text-align: justify;
			}
		}
	}
}
</style>
