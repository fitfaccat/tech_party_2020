<template>
	<section id="schedule">
		<h2>Cronograma</h2>

		<section class="content-talks">

			<nav class="menu-talks">
				<span class="active">27/Abril</span>
				<span>28/Abril</span>
				<span>29/Abril</span>
				<span>30/Abril</span>
			</nav>

			<section>
				<article class="talk">
					<div class="wrap-talk">
						<div class="wrap-info">
							<h2>Usando Windows no MacBook</h2>
							<div class="wrap-local">
								<div><span>Horário: 19:30</span></div>
								<div><span>Sala: B202</span></div>
							</div>
						</div>
						<p>
							Essa palestra explica como é fácil instalar o Windows em um simples MacBook, com apenas algum minutinhos você terá a bela tela azul em sua frente.
						</p>
					</div>
					<div class="wrap-perfil">
						<img src="https://pbs.twimg.com/profile_images/988775660163252226/XpgonN0X_400x400.jpg" alt="Bill Gates">
						<p>Bill Gates</p>
					</div>
				</article>
				<article class="talk">
					<div class="wrap-talk">
						<div class="wrap-info">
							<h2>Usando Windows no MacBook</h2>
							<div class="wrap-local">
								<div><span>Horário: 19:30</span></div>
								<div><span>Sala: B202</span></div>
							</div>
						</div>
						<p>
							Essa palestra explica como é fácil instalar o Windows em um simples MacBook, com apenas algum minutinhos você terá a bela tela azul em sua frente.
						</p>
					</div>
					<div class="wrap-perfil">
						<img src="https://pbs.twimg.com/profile_images/988775660163252226/XpgonN0X_400x400.jpg" alt="Bill Gates">
						<p>Bill Gates</p>
					</div>
				</article>
				<article class="talk">
					<div class="wrap-talk">
						<div class="wrap-info">
							<h2>Usando Windows no MacBook</h2>
							<div class="wrap-local">
								<div><span>Horário: 19:30</span></div>
								<div><span>Sala: B202</span></div>
							</div>
						</div>
						<p>
							Essa palestra explica como é fácil instalar o Windows em um simples MacBook, com apenas algum minutinhos você terá a bela tela azul em sua frente.
						</p>
					</div>
					<div class="wrap-perfil">
						<img src="https://pbs.twimg.com/profile_images/988775660163252226/XpgonN0X_400x400.jpg" alt="Bill Gates">
						<p>Bill Gates</p>
					</div>
				</article>
			</section>
		</section>
	</section>
</template>

<script>
export default {
  name: 'Schedule'
}
</script>

<style scoped lang="scss">
#schedule {
	width: 100%;
	height: 100vh;
	padding: 2rem;
	background: #0E0B16;
	color: #E7DFDD;

	h2 { padding-bottom: 2rem; }
	.content-talks {
		background: #E5E5E5;
		color: #0E0B16;
		height: 90%;
		display: flex;
		flex-direction: column;

		.menu-talks {
			width: 100%;
			display: flex;
			justify-content: space-around;

			.active {
				background: #E5E5E5;
				box-shadow: none;
			}
			span {
				box-shadow: inset 1px -2px 5px #0E0B16;
				background: #e84c3d;
				flex: 1;
				text-align: center;
				padding: 1rem 0;
				border-left: 2px solid #0E0B16;

				&:first-child {
					border-left: none;
				}
			}
		}
		section {
			overflow-y: auto;
			padding: .5rem 1rem;
		
			.talk {
				display: flex;
				border-bottom: 2px solid #C4C4C4;
				margin: 1rem 0;

				&:last-child {
					margin: 0;
					border-bottom: none;
				}
				.wrap-talk {
					flex: 3;

					.wrap-info {
						display: flex;

						h2,
						.wrap-local {
							display: flex;
							flex-direction: column;
							justify-content: center;
							padding: 1rem;
						}
						h2 {
							flex: 3;
							word-wrap: break-word;      /* IE 5.5-7 */
							white-space: -moz-pre-wrap; /* Firefox 1.0-2.0 */
							white-space: pre-wrap;
						}
						.wrap-local {
							flex: 1;
							position: relative;

							&::before {
								content: '';
								position: absolute;
								background: #0E0B16;
								height: 70%;
								top: 15%;
								left: 0;
								width: 2px;
							}
							div:first-child	{ margin-bottom: .25rem; }
						}
					}
					p {
						padding: 1rem;
						text-align: justify;
					}
				}
				.wrap-perfil {
					flex: 1;
					display: flex;
					flex-direction: column;
					justify-content: center;
					align-items: center;
					padding: 1rem 0;
					
					img {
						width: 160px;
						border-radius: 50%;
						border: 2px solid #e84c3d;
					}
					p { padding-top: .5rem; }
				}
			}
		}
	}
}
</style>
