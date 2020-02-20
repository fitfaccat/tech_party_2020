<template>
  <header :class="{ scroll: activeScroll }">
    <nav>
      <img src="https://techparty.faccat.br/images/logos/LogoTPtexto2.png" alt="Logo">
      <ul>
        <li><a href="#">INICIO</a></li>
        <li><a href="#speakers">PROGRAMAÇÃO</a></li>
        <li><a href="#">INSCRIÇÃO</a></li>
        <li><a href="#">SOBRE</a></li>
        <li><a href="#">PARCEIROS</a></li>
        <li><a href="#">LOCAL</a></li>    
      </ul>
    </nav>
    <div class="gradient-bottom"></div>
  </header>
</template>

<script>
export default {
  name: 'HeaderMenu',
  data() {
    return {
      activeScroll: false
    }
  },
  methods: {
    handleScroll () {
      const limitScroll = 100;
      if (window.scrollY > limitScroll) {
        return this.activeScroll = true;
      }
      return this.activeScroll = false;
    }
  },
  created () {
    window.addEventListener('scroll', this.handleScroll);
  },
  destroyed () {
    window.removeEventListener('scroll', this.handleScroll);
  }
}
</script>

<style scoped lang="scss">
$primary-color: #0E0B16;
$secundary-color: #E7DFDD;

$transition-timing-function: cubic-bezier(.52,.41,.81,.09);
$transition-duration: .1s;
$transition-delay: .1s;
$transition-delay: .1s;

header {
  display: flex;
  flex-direction: column;
  position: fixed;
  z-index: 99;
  width: 100%;
  transition:
    background-color
    $transition-duration
    $transition-timing-function
    $transition-delay;
          
  nav {
    background-color: ($primary-color + 'ff');
    padding: 0 1rem;
    display: flex;
    justify-content: space-between;

    img {
      height: 6rem;
      transition:
        height
        $transition-duration
        $transition-timing-function;
    }
    ul {
      display: flex;
      justify-content: space-around;
      align-items: center;

      li {
        padding: 0;
        color: $secundary-color;
        border-left: 1px solid $secundary-color;
        display: flex;
        align-items: center;
        justify-content: center;
        
        &:first-child { border: none; }
        a {
          margin: 0;
          width: 100%;
          height: 100%;
          color: $secundary-color;
          padding: .5rem 1.5rem;
          transition:
            background-color
            $transition-duration
            $transition-timing-function;

          &:hover{
            background-color: $secundary-color;
            color: $primary-color;
          }
        }
      }
    }
  }
}
.scroll {
  box-shadow: 0 10px 20px $primary-color;

  nav { background: $primary-color; }
  img { height: 4rem; }
}
</style>
