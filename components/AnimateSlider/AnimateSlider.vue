<template>


    <div class="hero-cryptogate justify-center pt-16 mt-16">
     
       <v-row justify="center" class="mb-12">
                <v-col md="10" sm="10" cols="10" lg="8">
     
           <vue-typed-js :strings="['Begginer', 'Trader','Everyone']" :loop="true" :cursorChar="'.'" :fadeOutDelay="2000" 	:typeSpeed="300">
  <h1 class="mb-6 text-h4 text-sm-h3 text-md-h2 text-xl-h2 text-lg-h3 font-weight-bold">Crypto App for you<span class="typing"></span></h1>
</vue-typed-js>
        <h6 class="mb-8 body-1 px-12 pt-3">Simple. Safe. Hassle-free.Starts from $ 1. Authorized payment gateway from prestigious specialized financial service providers </h6>
        <v-btn rounded depressed class="cryptogate-button text-center px-10 font-weight-regular mt-3" dark x-large>
          Start Investing Now
        </v-btn>
   
     
 
  
                  <v-img class="phone" max-width="800" position="center" :src="logo"></v-img>
    
              
      </v-col>
           </v-row>  
                   
      
       

         
    </div>
       

</template>

<style lang="scss">
  @import './hero';
</style>
<script>

  import ScrollWrap from '../ScrollWrap'
  import logo from '~/static/images/phone-crypto.png'
 import homeBg from '~/static/images/home-bg.svg'
  export default {
    components: {
      ScrollWrap
    
    },
    data() {
      return {
        homeBg: homeBg,
        logo: logo
      }
    }
  }

</script>
