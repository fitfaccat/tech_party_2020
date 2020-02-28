<template>
	<footer>
		<div class="footer-informations">
		<div id="footerInformations">
			<div id="footerSubscribe">
				<h1>TechParty 2020</h1>
				<button>INSCREVA-SE</button>
			</div>
			<div id="footerAbout">
				<h2>Mais sobre nós...</h2>
				<a href="">Conheça a FACCAT</a>
				<a href="">Conheça o curso de TI</a>
			</div>
		</div>
		<div id="footerLinks">
			<h2>Edições Anteriores (Sites)</h2>
			<a href="">Tech Party 2014</a>
			<a href="">Tech Party 2015</a>
			<a href="">Tech Party 2016</a>
			<a href="">Tech Party 2017</a>
			<a href="">Tech Party 2018</a>
			<a href="">Tech Party 2019</a>
		</div>
		<div id="footerSocialMedias">
			<div id="socialShare">
				<h2>Compartilhe</h2>
					<img src="../assets/f_logo_RGB-Blue_58.png" alt="">
					<a href="">@techpartyfaccat</a>
					<img src="../assets/Twitter_Social_Icon_Circle_Color.png" alt="">
					<a href="">@techpartyfaccat</a>
			</div>
			<div id="socialFollow">
				<h2>Siga-nos</h2>
				<img src="../assets/f_logo_RGB-Blue_58.png" alt="">
				<img src="../assets/Twitter_Social_Icon_Circle_Color.png" alt="">
				<img src="../assets/youtube_social_circle_red.png" alt="">
			</div>
			<div id="socialMail">
				<img src="https://ssl.gstatic.com/ui/v1/icons/mail/images/favicon5.ico" alt="">
				<a href="">techpartyfaccat@gmail.com</a>
			</div>
		</div>
		</div>
	</footer>
</template>

<script>
export default {
  name: 'FooterPage'
}
</script>

<style scoped lang="scss">
$primary-color: #0E0B16;
$secundary-color: #E7DFDD;
	
$transition-timing-function: cubic-bezier(.52,.41,.81,.09);
$transition-duration: .1s;
$transition-delay: .1s;

	footer{
		height: 60vh;
		padding: 1rem;
		
		.footer-informations{
			display: grid;
			background-color: $primary-color;
			grid-template-columns: 1fr 1fr 1fr;
			height: 100%;
		
		a{
			color:$secundary-color;
			&:hover{
				text-decoration: underline !important;
				text-decoration-color: $secundary-color;
			}
		}
		h1{color:$secundary-color;}
		h2{color:$secundary-color;}
		h3{color:$secundary-color;}
		
		div{padding: .1rem;}
		
		#footerInformations{
			align-content: center;
			justify-content: space-around;
			border-right: 1px solid $secundary-color;
			display: grid;
			grid-template-rows: 1fr 1fr;
			
			#footerSubscribe{
				display: grid;
				grid-template-rows: 1fr 1fr;
					background-color: $primary-color;
				
				button{
					width: 100%;
					background-color: $primary-color;
					color: $secundary-color;
					border: 1px solid $secundary-color;
					transition:
            background-color
            $transition-duration
            $transition-timing-function;
					
					&:hover{
						background-color: $secundary-color;
						color:$primary-color;
					}
				}
			}
			
			#footerAbout{
				margin: 1rem 0 0 0 ;
				display: grid;
				background-color: $primary-color;
				grid-template-rows: 1.5fr .75fr .75fr;
			}
		}
		
		#footerLinks{
				background-color: $primary-color;
			display: grid;
			grid-template-rows: 1.3fr .5fr .5fr .5fr .5fr .5fr .5fr;
			border-right: 1px solid $secundary-color;
			align-content: center;
			justify-content: space-around;
			
			h2{
				align-content: center;
				margin-top: 1rem;
			}
		}
		
		#footerSocialMedias{
			align-content: center;
			justify-content: space-around;
			display: grid;
			background-color: $primary-color;
			grid-template-rows: 1fr 1fr 1fr;
			
			#socialShare{
				display: grid;
				grid-template-rows: 1fr .5fr .5fr;
				#shareLinkOne{
					vertical-align: middle;
				}
				#shareLinkTwo{
					vertical-align: middle;
				}
				text-align: center;
				img{width: 32px;}
			}
			#socialFollow{
				text-align: center;
				img{
					width: 48px;
					margin: .5rem 2rem 0 0;
				}
			}
		}
			#socialMail{
				
			}
		}
	}
	
	
	
</style>
