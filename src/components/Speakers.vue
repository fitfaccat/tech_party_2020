<template>
	<section id="speakers">
		<h2>Palestrantes...</h2>
		<Speaker
			:key="id"
			v-for="(speaker, id) in speakers"
			:index="id"
			:name="speaker.name"
			:id="speaker.id"
			:image="speaker.image"
		/>
	</section>
</template>

<script>
import Speaker from './speakers/Speaker';

export default {
	name: 'Speakers',
	components: {
		Speaker
	},
	data() {
		return {
			speakers: [
				{
					name: 	"Bill Gates",
					id: 		"bill_gates",
					image:	"https://pbs.twimg.com/profile_images/988775660163252226/XpgonN0X_400x400.jpg"
				},
				{
					name: 	"Fausto Silva",
					id: 		"fausto_silva",
					image:	"https://pbs.twimg.com/profile_images/870982825/faust_o_400x400.gif"
				},
				{
					name: 	"Chuck Norris",
					id: 		"chuck_norris",
					image:	"https://sophosnews.files.wordpress.com/2012/01/chuck-norris-thumb.jpg?w=250"
				},
				{
					name: 	"Mark Zuckerberg",
					id: 		"mark_zuckerberg",
					image:	"https://imagens.canaltech.com.br/celebridades/539.400.jpg"
				},
				{
					name: 	"Jeff Bezos",
					id: 		"jeff_bezos",
					image:	"https://specials-images.forbesimg.com/imageserve/5bb22ae84bbe6f67d2e82e05/416x416.jpg?background=000000&cropX1=904&cropX2=1403&cropY1=262&cropY2=761"
				},
				{
					name: 	"Elon Musk",
					id: 		"elon_musk",
					image:	"https://www.biography.com/.image/t_share/MTY2MzU3Nzk2OTM2MjMwNTkx/elon_musk_royal_society.jpg"
				}
			]
		}
	}
}
</script>

<style scoped lang="scss">
@import './../assets/sass/variables.scss';

#speakers {
	width: 100%;
	padding: 2rem;
	background: $primary-color;

	h2 {
		padding-bottom: 2rem;
		color: $secundary-color;
	}
}
</style>
