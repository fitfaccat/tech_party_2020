<template>
	<section id="schedule">
		<h2>Cronograma</h2>
		<section class="content-talks">
			<tabs class="wrap-panel">
				<tab name="27/Abril" :selected="true" class="tab-panel">
					<ScheduleSpeaker
						title="Usando Windows no MacBook"
						hour="19:30"
						classroom="B202"
						description="Essa palestra explica como é fácil instalar o Windows em um simples MacBook, com apenas algum minutinhos você terá a bela tela azul em sua frente."
						:speaker="{
							name: 	'Bill Gates',
							id:			'bill_gates',
							image:	'https://pbs.twimg.com/profile_images/988775660163252226/XpgonN0X_400x400.jpg'
						}"
					/>
					<ScheduleSpeaker
						title="Domingão do TI"
						hour="20:30"
						classroom="B202"
						description="Faustão é um dos maiores apresentadores de televisão que o Brasil tem. Nessa talk descontraída, ele irá explicar como consegue prender a atenção do público com recursos de inteligência artificial."
						:speaker="{
							name: 	'Fausto Silva',
							id: 		'fausto_silva',
							image:	'https://pbs.twimg.com/profile_images/870982825/faust_o_400x400.gif'
						}"
					/>
				</tab>
				<tab name="28/Abril">
					<ScheduleSpeaker
						title="Windows Phone não morreu"
						hour="19:30"
						classroom="B202"
						description="Uma aposta, será que realmente não deu certo? Mr Bill nos conta detalhes estratégicos no mercado tecnológico que o fez retirar a versão mobile do Windows do planeta."
						:speaker="{
							name: 	'Bill Gates',
							id:			'bill_gates',
							image:	'https://pbs.twimg.com/profile_images/988775660163252226/XpgonN0X_400x400.jpg'
						}"
					/>
					<ScheduleSpeaker
						title="Debug correto"
						hour="20:30"
						classroom="B202"
						description='Aprenda de fato como "debugar" seu código com O Mestre, ele contará exclusivamente nessa noite como consegue realizar seus debugs no código apenas encarando ele, sim, o código não aguenta e confessa seu bug!'
						:speaker="{
							name: 	'Chuck Norris',
							id: 		'chuck_norris',
							image:	'https://sophosnews.files.wordpress.com/2012/01/chuck-norris-thumb.jpg?w=250'
						}"
					/>
				</tab>
				<tab name="29/Abril">
					<ScheduleSpeaker
						title="Muito mais likes"
						hour="19:30"
						classroom="B202"
						description="A história de como uma rede social se tornou uma das maiores e mais lucrativas empresas do mundo, influente com investimentos em tecnologia, o Facebook vai muito mais além que simples likes."
						:speaker="{
							name: 	'Mark Zuckerberg',
							id: 		'mark_zuckerberg',
							image:	'https://imagens.canaltech.com.br/celebridades/539.400.jpg'
						}"
					/>
					<ScheduleSpeaker
						title="Vou comprar você!"
						hour="20:30"
						classroom="B202"
						description='Sim, é apenas isso.'
						:speaker="{
							name: 	'Jeff Bezos',
							id: 		'jeff_bezos',
							image:	'https://specials-images.forbesimg.com/imageserve/5bb22ae84bbe6f67d2e82e05/416x416.jpg?background=000000&cropX1=904&cropX2=1403&cropY1=262&cropY2=761'
						}"
					/>
				</tab>
				<tab name="30/Abril">
					<ScheduleSpeaker
						title="Ao infinito... e além!"
						hour="19:30"
						classroom="B202"
						description='Conhecido como o Tony Stark da vida real, Elon Musk já contribuiu muito para a humanidade e hoje está a frente em um dos maiores projetos da história com a Space X, humanos estarão brevemente em Marte.'
						:speaker="{
							name: 	'Elon Musk',
							id: 		'elon_musk',
							image:	'https://www.biography.com/.image/t_share/MTY2MzU3Nzk2OTM2MjMwNTkx/elon_musk_royal_society.jpg'
						}"
					/>
					<ScheduleSpeaker
						title="É hora do churras!"
						hour="21:00"
						classroom="B202"
						description='Bora galeraaaaa!!! É hora do rango e daquele network com os melhores...'
					/>
				</tab>
			</tabs>
		</section>
	</section>
</template>

<script>
import Tabs from './tabulation/Tabs';
import Tab from './tabulation/Tab';
import ScheduleSpeaker from './schedule/ScheduleSpeaker';

export default {
	name: 'Schedule',
	components: {
		Tabs,
		Tab,
		ScheduleSpeaker
	}
}
</script>

<style scoped lang="scss">
@import './../assets/sass/variables.scss';

#schedule {
	width: 100%;
	height: 100vh;
	padding: 2rem;
	background: $primary-color;
	color: $secundary-color;

	h2 { padding-bottom: 2rem; }
	.content-talks {
		background: $secundary-color;
		color: $primary-color;
		height: 90%;
		
		.wrap-panel { height: 100%; }
	}
}
</style>
