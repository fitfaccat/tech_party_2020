<template>
	<section id="schedule">
		<h2>Cronograma</h2>

		<section class="content-talks">
			<tabs class="wrap-panel">
				<tab name="27/Abril" :selected="true" class="tab-panel">
					<article
						class="talk"
						v-for="n in 3"
						:key="n"
					>
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
						<a href="#" class="wrap-perfil">
							<img src="https://pbs.twimg.com/profile_images/988775660163252226/XpgonN0X_400x400.jpg" alt="Bill Gates">
							<p>Bill Gates</p>
						</a>
					</article>
				</tab>
				<tab name="28/Abril">
					<article
						class="talk"
						v-for="n in 2"
						:key="n"
					>
						<div class="wrap-talk">
							<div class="wrap-info">
								<h2>Teste</h2>
								<div class="wrap-local">
									<div><span>Horário: 19:30</span></div>
									<div><span>Sala: B202</span></div>
								</div>
							</div>
							<p>
								Essa palestra explica como é fácil instalar o Windows em um simples MacBook, com apenas algum minutinhos você terá a bela tela azul em sua frente.
							</p>
						</div>
						<a href="#" class="wrap-perfil">
							<img src="https://pbs.twimg.com/profile_images/988775660163252226/XpgonN0X_400x400.jpg" alt="Bill Gates">
							<p>Bill Gates</p>
						</a>
					</article>
				</tab>
				<tab name="29/Abril">
					<article
						class="talk"
						v-for="n in 3"
						:key="n"
					>
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
						<a href="#" class="wrap-perfil">
							<img src="https://pbs.twimg.com/profile_images/988775660163252226/XpgonN0X_400x400.jpg" alt="Bill Gates">
							<p>Bill Gates</p>
						</a>
					</article>
				</tab>
				<tab name="30/Abril">
					<article
						class="talk"
						v-for="n in 2"
						:key="n"
					>
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
						<a href="#" class="wrap-perfil">
							<img src="https://pbs.twimg.com/profile_images/988775660163252226/XpgonN0X_400x400.jpg" alt="Bill Gates">
							<p>Bill Gates</p>
						</a>
					</article>
				</tab>
			</tabs>

		</section>
	</section>
</template>

<script>
import Tabs from './tabulation/Tabs.vue';
import Tab from './tabulation/Tab.vue';

export default {
	name: 'Schedule',
	components: {
		Tabs,
		Tab
	}
}
</script>

<style scoped lang="scss">
$primary-color: #0E0B16;
$secundary-color: #E7DFDD;
$tertiary-color: #E84C3D;

$transition-timing-function: cubic-bezier(.52,.41,.81,.09);
$transition-duration: .1s;
$transition-delay: .1s;

#schedule {
	width: 100%;
	height: 100vh;
	padding: 2rem;
	background: $primary-color;
	color: $secundary-color;

	h2 { padding-bottom: 2rem; }
	.content-talks {
		background: #E5E5E5;
		color: $primary-color;
		height: 90%;
		
		.wrap-panel {
			height: 100%;
		
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
								background: $primary-color;
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
					color: $primary-color;
					transition:
            opacity
            $transition-duration
            $transition-timing-function;
					
					&:hover { opacity: .5; }
					img {
						width: 160px;
						border-radius: 50%;
						border: 2px solid $tertiary-color;
					}
					p { padding-top: .5rem; }
				}
			}
		}
	}
}
</style>
