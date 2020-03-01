<template>
  <v-app>
    <navbar></navbar>
   <intro/>
   <caroussel/>

   <h1 class="text-center font-weight-thin">Lorem ipsum dolor sit amet</h1>

    <card/>


<parallax/>

   <b-button variant="outline-info" v-on:click="show = !show" >View more</b-button>
  <div p v-if="show">
    <timeline></timeline>
  </div>  
<filtre/>

<commentaire/>

  <Footer/>

    <v-content>
    
    </v-content>
  </v-app>
</template>

<script>
import intro from './components/intro';
import timeline from './components/timeline';
import navbar from './components/navbar';
import Footer from './components/Footer';
import card from './components/card';
import caroussel from './components/caroussel';
import parallax from './components/parallax';
import commentaire from './components/commentaire';
import filtre from './components/filtre';


export default {
  name: 'App',

  components: {
    intro,
    timeline,
    navbar,
    Footer,
    card,
    caroussel,
    parallax,
    commentaire,filtre,

 
  },

  data: () => ({
     show: false
  }),

};

  </script>
