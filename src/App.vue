<template>
  <div id="app">

    <HeaderMenu />
    <Banner />
    <Speakers />
    <Subscribe />
    
  </div>
</template>

<script>
import HeaderMenu from './components/HeaderMenu.vue';
import Banner from './components/Banner.vue';
import Speakers from './components/Speakers.vue';
import Subscribe from './components/Subscribe.vue';

export default {
  name: 'App',
  components: {
    HeaderMenu,
    Banner,
    Speakers,
    Subscribe
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
  box-sizing: border-box;
  font-family: Consolas, Menlo, Monaco, Lucida Console, Liberation Mono, DejaVu Sans Mono, Bitstream Vera Sans Mono, Courier New, monospace, serif;
}
html, body { height: 100vh; }

#app {
  width: 100%;
  
  a { text-decoration: none; }
}

header {
  position: fixed;
  z-index: 99;
}
</style>
