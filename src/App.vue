<template>
  <div id="app">

    <HeaderMenu />
    <Banner />
    
  </div>
</template>

<script>
import HeaderMenu from './components/HeaderMenu.vue'
import Banner from './components/Banner.vue'

export default {
  name: 'App',
  components: {
    HeaderMenu,
    Banner
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
  font-family: Consolas, Menlo, Monaco, Lucida Console, Liberation Mono, DejaVu Sans Mono, Bitstream Vera Sans Mono, Courier New, monospace, serif;
}
#app {
  a { text-decoration: none; }
}

header {
  position: fixed;
  width: 100vw;
  z-index: 99;
}
</style>
