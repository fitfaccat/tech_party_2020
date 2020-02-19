<template>
  <header>
    <nav>
      <img src="https://techparty.faccat.br/images/logos/LogoTPtexto2.png" alt="Logo">
      <ul>
        <li><a href="#">INICIO</a></li>
        <li><a href="#">PROGRAMAÇÃO</a></li>
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
  name: 'HeaderMenu'
}
</script>

<style scoped lang="scss">
$primary-color: #0E0B16;
$secundary-color: #E7DFDD;
  
header {
  display: flex;
  flex-direction: column;
  position: fixed;
  z-index: 99;
  width: 100%;
          
  nav {
    background-color: ($primary-color + 'ff');
    padding: 0 1rem;
    display: flex;
    justify-content: space-between;
                
    img { height: 6rem; }
    ul {
      display: flex;
      justify-content: space-around;
      align-items: center;
      margin-right: 2rem;
                  
      li {
        color: $secundary-color;
        border-left: 1px solid $secundary-color;
                            
        &:first-child { border: none; }
        a {
          color: $secundary-color;
          padding: .5rem 1.5rem;
                                  
          &:hover{
            background-color: $secundary-color;
            color: $primary-color;
          }
        }
      }
    }
  }
  .gradient-bottom {
    background-color: transparent;
    background-image: linear-gradient(to bottom, $primary-color 5%, transparent);
    height: 50px;
    display: none;
  }
}
</style>
