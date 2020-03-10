<template>
	<section id="sponsors">
		<section id="becomeSponsor" class="fullhd-font-size">
			<span>{{ sessionData.sessions[0].content[0].text }}</span>
			<span class="email">
				{{ sessionData.sessions[0].content[1].text }}
			</span>
		</section>
		<section
			class="content-sponsor"
			v-for="(category, id) in sessionData.sessions"
			:key="id"
			v-show="id > 0"
		>
			<div :id="category.id" class="fullhd-font-size">
				<h1>{{ category.name }}</h1>
			</div>
			<article
				class="wrap-sponsor"
				:class="[(category.name == 'Bronze' || category.name == 'Apoio') ? `wrap-sponsor-${category.id}` : `wrap-sponsor-${category.id} fullhd-font-size`]"
				v-for="(sponsor, index) in category.content"
				:key="index"
				:id="sponsor.id"
			>
				<a :href="sponsor.link" target="_blank" >
					<figure>
						<img :src="sponsor.image" :alt="sponsor.title">
					</figure>
					<div class="description">
						<h2>{{ sponsor.title }}</h2>
						<p>
							{{ sponsor.text }}
						</p>
					</div>
				</a>
			</article>
		</section>
	</section>
</template>

<script>
export default {
	name: 'Sponsors',
	data() {
		return {
			sessionDataJson: `{"id":"sponsors","title":"Parceiros","sessions":[{"id":"seja_parceiro","name":"","description":"","content":[{"order":1,"link":"","image":"","text":"Seja você um patrocinador, entre em contato:"},{"order":2,"link":"","image":"","text":"techpartyfaccat@gmail.com"}]},{"id":"platinium","name":"Platinium","description":"","content":[{"order":1,"id":"rockstargames","link":"https://www.rockstargames.com/","image":"data:image/svg+xml,%3Csvg%20xmlns%3D%22http%3A%2F%2Fwww.w3.org%2F2000%2Fsvg%22%20viewBox%3D%220%200%20216%20198.83%22%3E%3Cdefs%3E%3Cstyle%3E.cls-1%7Bfill%3A%23fcaf17%3B%7D.cls-2%7Bfill%3A%23fff%3B%7D%3C%2Fstyle%3E%3C%2Fdefs%3E%3Ctitle%3EAsset%201%3C%2Ftitle%3E%3Cg%20id%3D%22Layer_2%22%20data-name%3D%22Layer%202%22%3E%3Cg%20id%3D%22Layer_1-2%22%20data-name%3D%22Layer%201%22%3E%3Cpath%20d%3D%22M214.55%2C197.37a4.94%2C4.94%2C0%2C1%2C1%2C1.45-3.5A4.75%2C4.75%2C0%2C0%2C1%2C214.55%2C197.37Zm-6.52-6.5a4.27%2C4.27%2C0%2C0%2C0%2C0%2C6%2C4.25%2C4.25%2C0%2C0%2C0%2C6%2C0%2C4.26%2C4.26%2C0%2C0%2C0-6-6Zm2.92.27a4.24%2C4.24%2C0%2C0%2C1%2C1.5.2%2C1.36%2C1.36%2C0%2C0%2C1%2C.84%2C1.38%2C1.17%2C1.17%2C0%2C0%2C1-.53%2C1.08%2C2.45%2C2.45%2C0%2C0%2C1-.78.26%2C1.32%2C1.32%2C0%2C0%2C1%2C.93.52%2C1.57%2C1.57%2C0%2C0%2C1%2C.3.84v.39c0%2C.13%2C0%2C.27%2C0%2C.41a1.2%2C1.2%2C0%2C0%2C0%2C0%2C.28l0%2C.07h-.89a.07.07%2C0%2C0%2C0%2C0%2C0s0%2C0%2C0-.07l0-.17v-.42c0-.63-.17-1.05-.52-1.24a2.45%2C2.45%2C0%2C0%2C0-1.07-.17H210v2.12h-.95v-5.43Zm1%2C.89a2.38%2C2.38%2C0%2C0%2C0-1.16-.2H210v1.94h.87a2.48%2C2.48%2C0%2C0%2C0%2C.93-.13A.94.94%2C0%2C0%2C0%2C212%2C192Z%22%2F%3E%3Cpath%20d%3D%22M178.43%2C0H38.26C17.17%2C0%2C0%2C16.66%2C0%2C37.12V161.63c0%2C20.74%2C16.65%2C37%2C37.91%2C37H178.08c21.26%2C0%2C37.92-16.26%2C37.92-37V37.12C216%2C16.31%2C199.5%2C0%2C178.43%2C0Zm33.31%2C161.62c0%2C18.36-14.78%2C32.75-33.66%2C32.75H37.91C19%2C194.37%2C4.25%2C180%2C4.25%2C161.62V37.11c0-18.43%2C15-32.86%2C34-32.86H178.43c18.68%2C0%2C33.31%2C14.43%2C33.31%2C32.86Z%22%2F%3E%3Cpath%20class%3D%22cls-1%22%20d%3D%22M178.43%2C4.25H38.26c-19.06%2C0-34%2C14.43-34%2C32.86V161.62C4.25%2C180%2C19%2C194.37%2C37.91%2C194.37H178.08c18.88%2C0%2C33.66-14.39%2C33.66-32.75V37.11C211.74%2C18.68%2C197.11%2C4.25%2C178.43%2C4.25Z%22%2F%3E%3Cpath%20d%3D%22M185.49%2C118.2H158.43l-4.29-27L138.28%2C118h-3a23.14%2C23.14%2C0%2C0%2C1-2.52-10.42c0-4.6.34-9.1.34-15%2C0-7.76-2.28-11.92-8.37-13.38V79c12.94-1.8%2C18.81-10.36%2C18.81-22.42%2C0-17.12-11.39-20.84-26.32-20.84H77.08l-17%2C80.4H81.45l6.18-29.25h14.19c7.57%2C0%2C10.67%2C3.7%2C10.67%2C10.79%2C0%2C5.39-.56%2C9.66-.56%2C13.81%2C0%2C1.54.35%2C5.11%2C1.38%2C6.49%2C0%2C0%2C15.43%2C16.29%2C15.43%2C16.29l-13.27%2C28.55L143.86%2C146%2C165%2C162.23l-4-26.93ZM108.2%2C71.86h-17L95.3%2C52.48h15.79c5.62%2C0%2C11.46%2C1.46%2C11.46%2C8.34C122.55%2C69.49%2C115.9%2C71.86%2C108.2%2C71.86Z%22%2F%3E%3Cpolygon%20class%3D%22cls-2%22%20points%3D%22173.03%20122.13%20155.08%20122.13%20151.97%20102.6%20140.53%20121.94%20122.42%20121.94%20133.43%20133.54%20124.38%20152.98%20144.16%20141.23%20159.74%20153.21%20156.84%20133.46%20173.03%20122.13%22%2F%3E%3C%2Fg%3E%3C%2Fg%3E%3C%2Fsvg%3E","title":"Rockstar Games","text":"Acima de tudo, é fundamental ressaltar que o aumento do diálogo entre os diferentes setores produtivos acarreta um processo de reformulação e modernização dos procedimentos normalmente adotados."},{"order":2,"id":"alphabet","link":"https://abc.xyz/","image":"https://abc.xyz/img/logo_2x.png","title":"Alphabet","text":"As experiências acumuladas demonstram que a constante divulgação das informações garante a contribuição de um grupo importante na determinação das novas proposições."}]},{"id":"gold","name":"Gold","description":"","content":[{"order":1,"id":"apple","link":"https://www.apple.com/","image":"https://www.apple.com/ac/globalnav/5/en_US/images/globalnav/apple/image_large.svg","title":"Apple","text":"Acima de tudo, é fundamental ressaltar que o aumento do diálogo entre os diferentes setores produtivos acarreta um processo de reformulação e modernização dos procedimentos normalmente adotados."},{"order":2,"id":"rocketchat","link":"https://rocket.chat/","image":"https://rocket.chat/images/default/logo.svg","title":"Rocket Chat","text":"As experiências acumuladas demonstram que a constante divulgação das informações garante a contribuição de um grupo importante na determinação das novas proposições."},{"order":3,"id":"nintendo","link":"https://www.nintendo.com/","image":"https://media.nintendo.com/share/nclood/stable/en-us/modules/nav/images/logo-nintendo.svg","title":"Nintendo","text":"As experiências acumuladas demonstram que a constante divulgação das informações garante a contribuição de um grupo importante na determinação das novas proposições."}]},{"id":"silver","name":"Silver","description":"","content":[{"order":1,"id":"spacex","link":"https://www.spacex.com/","image":"https://www.spacex.com/sites/spacex/files/spacex_logo_white.png","title":"SpaceX","text":"Acima de tudo, é fundamental ressaltar que o aumento do diálogo entre os diferentes setores produtivos acarreta um processo de reformulação e modernização dos procedimentos normalmente adotados."},{"order":2,"id":"tencent","link":"https://www.tencent.com/","image":"https://www.tencent.com/img/index/menu_logo.png","title":"Tencent腾讯","text":"As experiências acumuladas demonstram que a constante divulgação das informações garante a contribuição de um grupo importante na determinação das novas proposições."},{"order":3,"id":"oracle","link":"https://www.oracle.com/index.html","image":"data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='32' height='25' viewBox='0 0 32 25'%3E%3Cg fill='%23c74634'%3E%3Cpath d='M9.9,20.1c-5.5,0-9.9-4.4-9.9-9.9c0-5.5,4.4-9.9,9.9-9.9h11.6c5.5,0,9.9,4.4,9.9,9.9c0,5.5-4.4,9.9-9.9,9.9H9.9 M21.2,16.6c3.6,0,6.4-2.9,6.4-6.4c0-3.6-2.9-6.4-6.4-6.4h-11c-3.6,0-6.4,2.9-6.4,6.4s2.9,6.4,6.4,6.4H21.2'/%3E%3C/g%3E%3C/svg%3E","title":"Oracle","text":"As experiências acumuladas demonstram que a constante divulgação das informações garante a contribuição de um grupo importante na determinação das novas proposições."}]},{"id":"bronze","name":"Bronze","description":"","content":[{"order":1,"id":"dell","link":"https://www.dell.com/","image":"https://brand.delltechnologies.com/wp-content/uploads/2018/10/logoPg-Dell-300x210.png","title":"Dell","text":"Acima de tudo, é fundamental ressaltar que o aumento do diálogo entre os diferentes setores."},{"order":2,"id":"chucrechurros","link":"https://www.chucrechurros.com.br/","image":"https://www.chucrechurros.com.br/c-img/logo-chucre.png","title":"Chucrê Churros Gourmet","text":"As experiências acumuladas demonstram que a constante divulgação das informações garante a contribuição."}]},{"id":"apoio","name":"Apoio","description":"","content":[{"order":1,"id":"vigilianerd","link":"https://vigilianerd.com.br/","image":"https://vigilianerd.com.br/wp-content/themes/vigilia/images/logo-vigilia-nerd.png","title":"Vigília Nerd","text":"Acima de tudo, é fundamental ressaltar que o aumento do diálogo entre os diferentes setores produtivos."},{"order":2,"id":"alibaba","link":"https://www.alibaba.com/","image":"https://s.alicdn.com/@img/tfs/TB1pDDmmF67gK0jSZPfXXahhFXa-2814-380.png","title":"Alibaba.com","text":"As experiências acumuladas demonstram que a constante divulgação das informações garante a contribuição."}]}]}`
		};
	},
	computed: {
		sessionData() {
			console.log( JSON.parse(this.sessionDataJson) );
			return JSON.parse(this.sessionDataJson);
		}
	}
}
</script>

<style scoped lang="scss">
@import './../assets/sass/variables.scss';

#sponsors {
	margin: 2rem 0;

	#becomeSponsor {
		color: $secundary-color;
		text-align: center;
		padding: 6rem 0 1rem 0;

		.email { color: blue; }
	}
	.content-sponsor {
		display: flex;
		align-items: center;
		justify-content: center;
		flex-wrap: wrap;

		&:last-child {  margin-bottom: 10rem; }
		#platinium, #gold,
		#silver, #bronze,
		#apoio {
			width: 100%;
			padding: 1rem;
			margin-top: 2rem;
		}
		#platinium { background: $platinium; }
		#gold { background: $gold; }
		#silver { background: $silver; }
		#bronze { background: $bronze; }
		#apoio { background: $tertiary-color; }
		.wrap-sponsor {
			background-color: $secundary-color;
			margin: 0 1rem;
			margin-top: 2rem;
			border-radius: 1rem;
			overflow: hidden;
			border: 1px solid $secundary-color;
			transition:
				transform
				$transition-duration
				$transition-timing-function;
			
			&:hover {
				transform: scale(1.01);
				box-shadow: 2px 2px 20px #000;
			}
			a {
				color: $primary-color;
				height: 100%;
				display: flex;
				align-items: center;
				justify-content: center;
				border: none;
				
				figure {
					flex: 1;
					height: 100%;
					display: flex;
					align-items: center;
					justify-content: center;

					img {
						display: block;
						max-height: 100%;
						width: 75%;
					}
				}
				.description {
					flex: 1.5;
					padding: 4rem;

					p {
						padding: 1rem 0;
						text-align: justify;
					}
				}
			}
		}
		.wrap-sponsor-platinium {
			height: $full-height;
			width: 90%;
		}
		.wrap-sponsor-gold {
			height: ($full-height * 0.75); // 75%
			width: 45%;

			a .description { padding: 3rem; }
		}
		.wrap-sponsor-silver {
			height: ($full-height * 0.5); // 50%
			width: 45%;

			a .description { padding: 0 1rem; }
		}
		.wrap-sponsor-bronze,
		.wrap-sponsor-apoio {
			height: ($full-height * 0.25); // 25%
			width: 30%;
			font-size: 14px;

			a .description { padding: 0 1rem; }
			a .description p {  padding: .5rem 0; }
			h2 { font-size: 14px; }
		}
		#rockstargames {
			figure { background: $rockstargames-color; }
		}
		#alphabet {
			figure { background: $alphabet-color; }
		}
		#apple {
			figure { background: $apple-color; }
		}
		#rocketchat {
			figure { background: $rocketchat-color; }
		}
		#nintendo {
			figure { background: $nintendo-color; }
		}
		#spacex {
			figure { background: $spacex-color; }
		}
		#tencent {
			figure { background: $tencent-color; }
		}
		#oracle {
			figure { background: $oracle-color; }
		}
		#dell {
			figure { background: $dell-color; }
		}
		#chucrechurros {
			figure { background: $chucrechurros-color; }
		}
		#vigilianerd {
			figure { background: $vigilianerd-color; }
		}
		#alibaba {
			figure { background: $alibaba-color; }
		}
	}
}

/* responsive */
@media (max-width: 1300px) {
	#sponsors .content-sponsor {
		.wrap-sponsor-bronze,
		.wrap-sponsor-apoio {
			width: 40%;
		}
	}
}
@media (max-width: 1000px) {
	#sponsors .content-sponsor {
		.wrap-sponsor-silver,
		.wrap-sponsor-gold {
			width: 75%;
		}
		.wrap-sponsor-bronze,
		.wrap-sponsor-apoio {
			width: 50%;
		}
	}
}
@media (max-width: 800px) {
	#sponsors .content-sponsor {
		.wrap-sponsor a figure img {
			width: initial;
			max-width: 75%;
		}
		.wrap-sponsor-bronze,
		.wrap-sponsor-apoio {
			width: 75%;
		}
	}
}
@media (max-width: 650px) {
	#sponsors {
		#becomeSponsor {
			padding: 1rem;
		}
		.content-sponsor {
			.wrap-sponsor a .description {
				padding: 2rem;
			}
			.wrap-sponsor-silver,
			.wrap-sponsor-gold,
			.wrap-sponsor-bronze,
			.wrap-sponsor-apoio {
				width: 90%;
			}
		}
	}
}
</style>
