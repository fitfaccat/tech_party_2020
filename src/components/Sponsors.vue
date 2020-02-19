<template>
	<section>
		<div id="becomeSponsor">
			SEJA VOCÊ UM PATROCINADOR, ENTRE EM CONTATO: TECHPARTYFACCAT@GMAIL.COM
		</div>
		<section id="platinum">
			<h2>PLATINUM</h2>
			<article>
				<div id="imagemPlatinum">
					<img src="#" alt="">
				</div>
				<div id="textoPlatinum">
					<h3>PADARIA DO SEU ZÈ</h3>
					<p>Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum</p>	
				</div>
			</article>
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
	
	section{
		background-color: red;
		
		#becomeSponsor{
			display: flex;
			justify-content: space-around;
			text-align: center;
			height: 2.5rem;
			padding: 2.5rem;
		}
		
		#platinum{	
			h2{
				display: flex;
				background-color: blue;
				height: 2rem;
				text-align: center;
				justify-content: space-around;
			}
			article{	
				display: flex;
				flex-direction:row;
				#imagemPlatinum{
					height: 5rem;
					width: 5rem;
					background: yellow;
				}
				#textoPlatinum{
					
				}
			}
		}
		
	}
    
</style>
