<template>
  <div id="app">
		<HeaderMenu/>
		<Sponsors/>
  </div>
</template>

<script>
import HeaderMenu from './components/HeaderMenu.vue'
import Sponsors from './components/Sponsors.vue'
		
export default {
  name: 'App',
  components: {
    HeaderMenu,
		Sponsors
  }
}
</script>

<style lang="scss">
* {
    padding: 0;
    margin: 0;
    vertical-align: baseline;
    list-style: none;
    border: 0;
}
#app {
    a { text-decoration: none; }
}
</style>
