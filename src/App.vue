<template>
  <div id="app">

    <HeaderMenu />
    <Banner />
    <Schedule />
    <Speakers />
    <Subscribe />
    <About />
    <Sponsors />
    <Churras />
    <Local />
    <FooterPage/>
    
  </div>
</template>

<script>
	
import HeaderMenu from './components/HeaderMenu.vue';
import Banner from './components/Banner.vue';
import Schedule from './components/Schedule.vue';
import Speakers from './components/Speakers.vue';
import Subscribe from './components/Subscribe.vue';
import About from './components/About';
import Sponsors from './components/Sponsors.vue'
import Churras from './components/Churras.vue';
import Local from './components/Local.vue';
import FooterPage from './components/FooterPage.vue';
	
export default {
  name: 'App',
  components: {
    HeaderMenu,
    Schedule,
    Banner,
    Speakers,
    Subscribe,
    About,
    Sponsors,
    Churras,
    Local,
		FooterPage
  }
}
</script>

<style lang="scss">
@import './assets/sass/variables.scss';

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
  background-color: $primary-color;

  a { text-decoration: none; }
}
</style>
