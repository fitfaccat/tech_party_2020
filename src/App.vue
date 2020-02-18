<template>
  <div id="app">
    <HeaderMenu/>
  </div>
</template>

<script>
import HeaderMenu from './components/HeaderMenu.vue'

export default {
  name: 'App',
  components: {
    HeaderMenu
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
