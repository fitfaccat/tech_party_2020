<template>
	<article class="talk">
		<div class="wrap-talk">
			<div class="wrap-info">
				<h2>{{ title }}</h2>
				<div class="wrap-local">
					<div><span>Horário: {{ hour }}</span></div>
					<div><span>Sala: {{ classroom }}</span></div>
				</div>
			</div>
			<p>{{ description }}</p>
		</div>
		<a
			class="wrap-perfil"
			v-if="speaker"
			:href="'#' + speaker.id"
		>
			<img :src="speaker.image" :alt="speaker.name">
			<p>{{ speaker.name }}</p>
		</a>
	</article>
</template>

<script>
export default {
	name: 'ScheduleSpeaker',
	props: {
		title: 				String,
		hour: 				String,
		classroom: 		String,
		description:	String,
		speaker:			Object
	}
}
</script>

<style scoped lang="scss">
@import './../../assets/sass/variables.scss';

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

/* responsive */
@media (max-width: 600px) {
	.talk { flex-direction: column-reverse; }
}
</style>
