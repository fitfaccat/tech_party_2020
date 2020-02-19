<template>
	<section>
		<div id="becomeSponsor">
			SEJA VOCÊ UM PATROCINADOR, ENTRE EM CONTATO: TECHPARTYFACCAT@GMAIL.COM
		</div>
			<section id="conteinerPlatinum">
				<h2>PLATINUM</h2>
				<div id="conteinerArticlePlatinum">
					<article>
						<div id="imagePlatinum">
							<img src="#" alt="">
						</div>
						<div id="textPlatinum">
							<h3>PADARIA DO SEU ZÈ</h3>
							<p>Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum.<br><br>Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum</p>	
						</div>
					</article>
				</div>
		</section>
		<section id="conteinerGold">
			<h2>GOLD</h2>
				<div id="conteinerGoldArticles">
					<div id="conteinerArticleGold">
						<article>
							<div id="imageGold">
								<img src="#" alt="">
							</div>
							<div id="textGold">
								<h3>PADARIA DO SEU ZÈ</h3>
								<p>Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum.</p>	
							</div>
						</article>
					</div>
					<div id="conteinerArticleGold">
						<article>
							<div id="imageGold">
								<img src="#" alt="">
							</div>
							<div id="textGold">
								<h3>PADARIA DO SEU ZÈ</h3>
								<p>Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum.</p>	
							</div>
						</article>
					</div>
			</div>
		</section>
	</section>
</template>

<script>
export default {
	name: 'Sponsors'
}
</script>

<style scoped lang="scss">
	$primary-color:#0E0B16;
  $secundary-color: #E7DFDD;
	$h3font-size: 2rem;
	
	section{
		background-color: $primary-color;
		
		#becomeSponsor{
			display: flex;
			justify-content: space-around;
			text-align: center;
			height: 2.5rem;
			padding: 2.5rem;
			color: $secundary-color;
		}
		
		#conteinerPlatinum{	
			
			h2{
				display: flex;
				background-color: silver;
				height: 2rem;
				text-align: center;
				justify-content: space-around;
			}
			#conteinerArticlePlatinum{
				padding: 1rem;
				background-color: $secundary-color;
				display: flex;
				margin: 1rem 1rem;
				
				article{
					margin: 0rem 3rem;
					display: grid;
					grid-template-columns: 1fr 2fr;
					
					#imagePlatinum{
						height: 100vh 100%;
						background: yellow;
						justify-content: space-around;
					}
					
					#textPlatinum{
						h3{
							display: flex;
							text-align: center;
							justify-content: space-around;
							font-size: $h3font-size;
						}
						p{
							align-content: center;
							text-align:left;
							margin-left: 10px;
						}
					
					}
				}
			}
		
		}
	}
	#conteinerGold{
		h2{
				display: flex;
				background-color: gold;
				height: 2rem;
				text-align: center;
				justify-content: space-around;
			}
		#conteinerGoldArticles{
			display: grid;
			grid-template-columns: 1fr 1fr;
			#conteinerArticleGold{
					padding: 1rem;
					background-color: $secundary-color;
					display: flex;
					margin: 1rem 1rem;
				
					article{
						margin: 0;
						display: grid;
						grid-template-columns: 1fr 2fr;
					
						#imageGold{
							height: 15rem;
							width: 15rem;
							background: yellow;
							justify-content: space-around;
						}
					
						#textGold{
							h3{
								display: flex;
								text-align: center;
								justify-content: space-around;
								font-size: $h3font-size;
							}
							p{
								align-content: center;
								text-align:left;
								margin-left: 10px;
						}
					}
				}
			}
		}
	}
</style>
