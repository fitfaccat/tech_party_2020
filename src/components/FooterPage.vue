<template>
	<footer>
		<section class="content">
			<article>
				<h2>TechParty 2020</h2>
				<a href="https://saga2.faccat.br/index.php?op=1068&chave=1739&portal=E" class="subscribe" target="_blank">
					<button>
						INSCREVA-SE
					</button>
				</a>
				<h3>Mais sobre nós...</h3>
				<div class="link-access">
					<a href="http://www.faccat.br/" target="_blank">Conheça a FACCAT</a>
				</div>
				<div class="link-access">
					<a href="http://fit.faccat.br/" target="_blank">Conheça os cursos de TI</a>
				</div>
				<div class="link-access">
					<a href="https://www.facebook.com/TiFaccat/" target="_blank">Siga a TI Faccat no Facebook</a>
				</div>
			</article>
			<article>
				<h3>Edições Anteriores</h3>
				<div class="link-access">
					<a href="https://techparty.faccat.br/2014/" target="_blank">Tech Party 2014</a>
				</div>
				<div class="link-access">
					<a href="https://techparty.faccat.br/2015/" target="_blank">Tech Party 2015</a>
				</div>
				<div class="link-access">
					<a href="https://techparty.faccat.br/2016/" target="_blank">Tech Party 2016</a>
				</div>
				<div class="link-access">
					<a href="https://techparty.faccat.br/2017/" target="_blank">Tech Party 2017</a>
				</div>
				<div class="link-access">
					<a href="https://techparty.faccat.br/2018/" target="_blank">Tech Party 2018</a>
				</div>
				<div class="link-access">
					<a href="https://techparty.faccat.br/2019/" target="_blank">Tech Party 2019</a>
				</div>
			</article>
			<article>
				<h3>Compartilhe</h3>
				<div class="share-social">
					<a href="https://www.facebook.com/sharer.php?u=https://www.facebook.com/techpartyfaccat/" class="link-access" target="_blank">
						<img class="small" src="../assets/f_logo_RGB-Blue_58.png" alt="">
						<span>@techpartyfaccat</span>
					</a>
					<a href="https://twitter.com/share?url=https://twitter.com/techpartyfaccat&text=T%C3%B4%20na%20Faccat%20curtindo%20e%20aprendendo%20na" class="link-access" target="_blank">
						<img class="small" src="../assets/Twitter_Social_Icon_Circle_Color.png" alt="">
						<span>@techpartyfaccat</span>
					</a>
				</div>
				<h3>Siga-nos</h3>
				<div class="share-social share">
					<a href="https://www.facebook.com/techpartyfaccat/" target="_blank">
						<img src="../assets/f_logo_RGB-Blue_58.png" alt="">
					</a>
					<a href="https://twitter.com/techpartyfaccat" target="_blank">
						<img src="../assets/Twitter_Social_Icon_Circle_Color.png" alt="">
					</a>
					<a href="https://www.youtube.com/playlist?list=PLkLwxRNpclbghZcA2PYzLyAbvKR3qZuam" target="_blank">
						<img src="../assets/youtube_social_circle_red.png" alt="">
					</a>
				</div>
				<div class="share-social share">
					<a href="mailto:techpartyfaccat@gmail.com" class="link-access" target="_blank">
						<img class="small" src="https://ssl.gstatic.com/ui/v1/icons/mail/images/favicon5.ico" alt="">
						<span>techpartyfaccat@gmail.com</span>
					</a>
				</div>
			</article>
		</section>
		<section class="content-footer">
			<img src="../assets/tech-party.png" alt="">
			<a href="https://github.com/fitfaccat/tech_party_2020" target="_blank">
				<span>tech_party_2020</span>
				<img src="../assets/GitHub-Mark-32px.png" alt="">
			</a>
		</section>
	</footer>
</template>

<script>
export default {
  name: 'FooterPage'
}
</script>

<style scoped lang="scss">
@import './../assets/sass/variables.scss';

footer {
	background: $primary-color;
	color: $secundary-color;
	height: 50vh;

	a { color: $secundary-color; }
	img { width: 32px; margin-right: .5rem; }
	.content {
		height: 50vh;
		display: flex;
		align-items: center;

		article {
			flex: 1;
			padding: 0 2rem;
			
			.link-access {
				margin: .25rem 0;
				a:hover { border-bottom: 1px solid $secundary-color; }
			}
			.subscribe {
				display: flex;
				justify-content: center;
				border-bottom: none;

				button {
					margin: 1rem 0;
					border: 2px solid $secundary-color;
					padding: 1rem 2rem;
					color: $secundary-color;
					font-weight: bold;
					font-size: 18px;
					border-radius: 1rem;
					background-color: $primary-color;
					cursor: pointer;
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
			.share-social {
				margin-bottom: 1rem;
				display: flex;

				a {
					display: flex;
					align-items: center;

					span { margin-right: 1rem; }
				}
				.small {
					width: 16px;
					height: 16px;
				}
			}
			.share { justify-content: flex-start; }
		}
	}
	.content-footer {
		height: 10vh;
		background: $tertiary-color;
		display: flex;
		align-items: center;
		justify-content: space-between;

		img { margin: 0 1rem; }
		a {
			display: flex;
			align-items: center;
			justify-content: space-between;
			color: $tertiary-color-shade;

			&:hover { color: $secundary-color; }
		}
	}
}
</style>
