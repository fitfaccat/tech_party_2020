<template>
	<section class="wrap-images">
		
		<slot></slot>

	</section>	
</template>

<script>
export default {
	name: 'Gallery'
}
</script>

<style scoped lang="scss">
@import './../../assets/sass/variables.scss';

.wrap-images {
	width: 100%;
	height: 90vh;
}
</style>