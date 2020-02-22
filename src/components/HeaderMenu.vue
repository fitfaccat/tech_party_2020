<template>
  <header :class="{ scroll: activeScroll }">
    <nav>
      <img src="https://techparty.faccat.br/images/logos/LogoTPtexto2.png" alt="Logo">

      <div
        class="menu-bar"
        :class="{ active: activeMenu }"
        @click="spinMenu"
      >
        <svg viewBox="0 0 100 100">
          <path d="M0, 20 Q50, 20 100, 20"></path>
          <path d="M0, 40 Q50, 40 100, 40"></path>
          <path d="M0, 60 Q50, 60 100, 60"></path>
          <path d="M0, 80 Q50, 80 100, 80"></path>
        </svg>
      </div>

      <ul
        class="menu-list"
        :class="{ openMenu: activeMenu }"
      >
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
      activeScroll: false,
      activeMenu:   false
    }
  },
  methods: {
    handleScroll () {
      const limitScroll = 100;
      if (window.scrollY > limitScroll) {
        return this.activeScroll = true;
      }
      return this.activeScroll = false;
    },
    spinMenu() {
      this.activeMenu = !this.activeMenu;
      return this.activeMenu;
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
@import './../assets/sass/variables.scss';

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
    align-items: center;

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
        user-select: none;
        padding: 0;
        color: $secundary-color;
        border-left: 1px solid $secundary-color;
        display: flex;
        align-items: center;
        justify-content: center;
        
        &:first-child { border-left: none; }
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

/* responsive */
@media (max-width: 1000px) {
  header {
    nav { padding: 0; }
  }
}
@media (max-width: 965px) {
  header {
    nav {
      position: relative;

      ul { display: none; }
      .menu-list {
        display: flex;
        justify-content: center;
        align-items: center;
        flex-direction: column;
        width: 64%;
        height: 100vh;
        background: $tertiary-color;
        position: absolute;
        top: 0;
        right: 0;
        z-index: 99;
        box-shadow: 0 5px 20px $primary-color;
        overflow-y: auto;
        transform: translateX(110%);
        transition:
          transform
          $transition-duration
          $transition-timing-function;

        li {
          border-left: none;
          border-bottom: 1px solid $secundary-color;
          width: 90%;
          text-align: left;
          padding: .5rem 0;

          &:hover{ background-color: $secundary-color; }
          a {
            transition: none;
            transition:
              transform
              $transition-duration
              $transition-timing-function;
            &:hover {
              transform: translateX(1px);
              background-color: initial;
            }
          }
        }
      }
      .openMenu { transform: translateX(0); }
      .menu-bar {
        position: absolute;
        right: 0;
        top: 0;
        display: flex;
        align-items: center;
        justify-content: center;
        padding: 0 1rem;
        border: 0;
        border-radius: .5rem;
        background: $tertiary-color;
        margin: .7rem 1rem;
        height: 2.5rem;
        z-index: 100;
      
        svg {
          width: 20px;
          height: 20px;
          overflow: visible;
          display: block;

          path {
            fill: none;
            stroke-width: 8;
            stroke: $secundary-color;
            transition: 0.4s;
          }
        }
      }
      .active {
        svg {
          border-radius: 50%;
          animation: 
            logspin 1.5s linear infinite,
            logglow 1.25s ease infinite alternate;
        }
        path {
          &:nth-child(1) { d: path("M50, 0 Q100, 0 100,50"); }
          &:nth-child(2) { d: path("M100, 50 Q100, 100 50,100"); }
          &:nth-child(3) { d: path("M50,100 Q0, 100 0, 50"); }
          &:nth-child(4) { d: path("M0, 50 Q0, 0 50, 0"); }
        }
      }
    }
  }
}

/* keyframe */
@keyframes logspin {
  100% { transform: rotate(360deg); }
}
@keyframes logglow {
  100% { box-shadow: 0 0 5px 2px $tertiary-color; }
}
</style>
