<template>
    <header>
        <div class="div1">
        <img src="https://techparty.faccat.br/images/logos/LogoTPtexto2.png" alt="Logo">
        <ul >
           <li><a href="">INICIO</a></li>
            <li><a href="">PROGRAMAÇÃO</a></li>
             <li><a href="">INSCRIÇÃO</a></li>
             <li><a href="">SOBRE</a></li>
             <li><a href="">PARCEIROS</a></li>
            <li><a href="">LOCAL</a></li>    
        </ul>
    </div>
    <div class="div2"></div>
    </header>
</template>

<script>
export default {
  name: 'HeaderMenu'
}
</script>

<style scoped lang="scss">
    $primary-color:#0e0b16;
    $secundary-color: #E7DFDD;
    header {
        display: flex;
        flex-direction: column;
        .div1 {
            background-color: $primary-color;
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
                    padding: 1rem 1.5rem;
                    border-left: 1px solid $secundary-color;
                    color: $secundary-color;
                    &:first-child { border: none; }
                
                    a {color: $secundary-color;}
                    
                    a:hover{
                        padding: 2px;
                        background-color: $secundary-color;
                        border-radius: 3px;
                        color: $primary-color;
                        border: 3px  outset $secundary-color;
                    }
                }
            }
        }
        .div2 {
            background-color: transparent;
            background-image: linear-gradient(to bottom, $primary-color 5%, transparent);
            height: 50px;
            display: flex;
        }
    }
</style>
