<template>
	<div class="countdown">
		<div class="wrap">
			<span class="item-top" id="days"></span>
			<span class="item-bottom">Dias</span>
		</div>
		<div class="wrap">
			<span class="item-top" id="hours"></span>
			<span class="item-bottom">Horas</span>
		</div>
		<div class="wrap">
			<span class="item-top" id="minutes"></span>
			<span class="item-bottom">Minutos</span>
		</div>
		<div class="wrap">
			<span class="item-top" id="seconds"></span>
			<span class="item-bottom">Segundos</span>
		</div>
	</div>
</template>

<script>
export default {
	name: 'Countdown',
	props: {
		dateEvent: String
	},
	created() {
		const second = 1000,
			minute = second * 60,
			hour = minute * 60,
			day = hour * 24;

		let countDown = parseInt(this.dateEvent, 10);

		setInterval(function() {
			let now = new Date().getTime(),
				distance = countDown - now;
				document.getElementById('days').innerText = Math.floor(distance / (day)),
				document.getElementById('hours').innerText = Math.floor((distance % (day)) / (hour)),
				document.getElementById('minutes').innerText = Math.floor((distance % (hour)) / (minute)),
				document.getElementById('seconds').innerText = Math.floor((distance % (minute)) / second);
		}, second)
	}
}
</script>

<style scoped lang="scss">
@import url('https://fonts.googleapis.com/css?family=Roboto+Mono:700&display=swap');
@import './../../assets/sass/variables.scss';

.countdown {
	margin: 1rem;
	font-family: 'Roboto Mono', monospace;
	width: 50%;
	display: flex;
	align-items: center;
	justify-content: center;

	.wrap {
		flex: 1;
		margin: 0.5rem;
		display: flex;
		flex-direction: column;
		align-items: center;

		.item-bottom,
		.item-top {
			color: $tertiary-color;
		}
		.item-top {
			font-weight: bold;
			font-size: 64px;
		}
	}
}

@media (max-width: 1000px) {
	.countdown { width: 75%; }
}
@media (max-width: 600px) {
	.countdown {
		width: 100%;
		.wrap {
			.item-top { font-size: 28px; }
			.item-bottom { font-size: 16px; }
		}
	}
}
</style>