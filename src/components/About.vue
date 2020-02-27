<template>
	<section id="about">
		
		<article>
			<h2>SOBRE</h2>
			<p>
				A TechParty é um evento que visa promover a tecnologia (Tech) durante um evento informal e de congregação (Party). Os organizadores convidam profissionais experientes da área de TI (Tecnologia da Informação) para apresentações curtas (normalmente de até 40 minutos). Desenvolvimento de software e hardware, linguagens e ferramentas, metodologias, tudo que envolva TI nos interessa. Normalmente são duas apresentações por noite, mas com intervenções rápidas antes e no meio das apresentações realizadas pelos patrocinadores e parceiros que fazem rápidos sorteios de brindes, apresentam suas empresas, entre outras atividades. Ao fim de cada noite todos os participantes são convidados a participarem do RangoBreak, que é uma espécie de coffee break mais, digamos, “reforçado” :D. Esse RangoBreak é gratuito a todos os participantes e pode ser oferecido graças ao apoio dos nossos incríveis patrocinadores (obrigado!).
			</p>
			<p>
				O evento é aberto ao público em geral e totalmente gratuito, incluindo o RangoBreak, que é o nosso momento de integração e networking. Todos os participantes ganham certificado emitido pela Faccat (essas horas podem contar como Atividades Complementares). De certa forma, essa semana da TechParty pode ser considerada a Semana Acadêmica dos Cursos da Área de TI da Faccat.
			</p>
			<h2>O SURGIMENTO</h2>
			<p>
				Tudo iniciou em 2011 pela iniciativa de um grupo de alunos do curso de Sistemas de Informação da Faccat. Era totalmente organizado por esses alunos e ocorria uma vez por semestre em finais de semanas, com palestras e minicursos para leigos até usuários avançados de computação. Contava com apresentações de profissionais de fora da instituição e, também, apresentações feitas pelos próprios alunos e professores. Essas atividades aconteceram ao longo de 2011 e 2012. Por indisponibilidades diversas, em 2013 o evento não aconteceu.
			</p>
			<h3>Veja como foi nos anos anteriores!</h3>
			<aside>
				<svg class="arrows">
					<path class="a1" d="M0 0 L30 32 L60 0"></path>
					<path class="a2" d="M0 20 L30 52 L60 20"></path>
					<path class="a3" d="M0 40 L30 72 L60 40"></path>
				</svg>
			</aside>
		</article>

		<gallery>
			<div class="images">
				<div class="title">
					<h2>2014</h2>
					<h3>Vira um evento anual</h3>
				</div>
				<div class="text">
					<p>
						Em 2014, estudantes da instituição com o objetivo de oferecer conhecimento para o maior número de pessoas, optam por retornar com o evento, mas agora com organização diferenciada.
					</p>
					<p>
						TechParty passou a ser um evento anual, com duração de uma semana inteira, com duas talks (apresentações) por noite e coffee break atraente a fim de estimular a interação das pessoas e o networking. Mantendo a proposta de contar com palestrantes da faculdade e convidados externos, mas sempre com assuntos interessantes e atuais, o evento teve um salto no número de participantes com esse novo formato, ultrapassando 700 pessoas (somadas as 5 noites), entre alunos, ex-alunos, pessoas da comunidade, alunos de escolas da região e representantes de muitas empresas da área de atuação da Faccat.
					</p>
				</div>
				<!-- <img
					v-for="(x, id) in 7"
					:key="id"
					:src="`./../2014/${x}.jpg`" alt=""
				> -->
				<figure class="a"></figure>
				<figure class="b"></figure>
				<figure class="c"></figure>
				<figure class="d"></figure>
				<figure class="e"></figure>
				<figure class="f"></figure>
				<figure class="g"></figure>
				<figure class="h"></figure>
			</div>
		</gallery>

		<gallery>
			<p>2015</p>
		</gallery>

		<gallery>
			<p>2016</p>
		</gallery>

		<gallery>
			<p>2017</p>
		</gallery>

		<gallery>
			<p>2018</p>
		</gallery>

		<gallery>
			<p>2019</p>
		</gallery>


	</section>
</template>

<script>
import Gallery from './gallery/Gallery';

export default {
	name: 'About',
	components: {
		Gallery
	}
}
</script>

<style scoped lang="scss">
@import './../assets/sass/variables.scss';


#about {
	background: $secundary-color;
	color: $primary-color;
	width: 100%;

	.images {
		height: 100%;
		width: 100%;
		padding: 1rem;
		position: relative;
		border-bottom: 1px solid;

		.text,
		.title {
			background: #ffffffaa;
			position: absolute;
			padding: 2rem;
			z-index: 80;

			h2 { font-size: 48px; }
			p {
				margin-top: 1rem;
				&:first-child { margin-top: 0; }
			}
		}
		.title {
			bottom: 10%;
			left: 6%;
			text-align: center;
		}
		.text {
			top: 10%;
			right: 5%;
			width: 75%;
			text-align: justify;
		}

		figure {
			border: 1px solid darkmagenta;
			width: 100px;
			height: 100px;
			position: absolute;
		}
		.a {
			background: darkmagenta;
			top: 2%;
			left: 2%;
			width: 34%;
			height: 30%;
		}
		.b {
			background: darkolivegreen;
			top: 2%;
			left: 38%;
			width: 34%;
			height: 60%;
		}
		.c {
			background: darkred;
			top: 2%;
			right: 2%;
			width: 24%;
			height: 45%;
		}
		.d {
			background: darkslategray;
			bottom: 2%;
			left: 2%;
			width: 34%;
			height: 64%;
		}
		.e {
			background: darkcyan;
			bottom: 2%;
			left: 38%;
			width: 24%;
			height: 34%;
		}
		.f {
			background: darkblue;
			bottom: 2%;
			right: 2%;
			width: 34%;
			height: 20%;
		}
		.g {
			background: darkorange;
			bottom: 24%;
			right: 2%;
			width: 24%;
			height: 27%;
		}
		.h {
			background: deepskyblue;
			bottom: 24%;
			right: 28%;
			width: 8%;
			height: 12%;
		}
	}

	article {
		padding: 4rem;
	
		h2,
		h3,
		p { padding: 1rem 0; }
		p { text-align: justify; }
	}
	aside {
		width: 100%;
		display: flex;
		justify-content: center;

		.arrows {
			width: 60px;
			height: 72px;

			path {
				stroke: $primary-color;
				fill: transparent;
				stroke-width: 1px;	
				animation:
					arrow
					2s
					infinite;
				-webkit-animation:
					arrow
					2s
					infinite; 
			}
			path.a1 {
				animation-delay: -1s;
				-webkit-animation-delay: -1s; /* Safari 和 Chrome */
			}
			path.a2 {
				animation-delay: -0.5s;
				-webkit-animation-delay: -0.5s; /* Safari 和 Chrome */
			}
			path.a3 {	
				animation-delay: 0s;
				-webkit-animation-delay: 0s; /* Safari 和 Chrome */
			}
		}
	}

}

@keyframes arrow {
	0% {opacity:0}
	40% {opacity:1}
	80% {opacity:0}
	100% {opacity:0}
}
@-webkit-keyframes arrow /*Safari and Chrome*/ {
	0% {opacity:0}
	40% {opacity:1}
	80% {opacity:0}
	100% {opacity:0}
}
</style>