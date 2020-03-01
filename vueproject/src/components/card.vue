<template>
  <v-container class="pa-4 text-center">
    <v-row class="fill-height" align="center" justify="center">
      <template v-for="(item, i) in items">
        <v-col
          :key="i"
          cols="12"
          md="4"
        >
          <v-hover v-slot:default="{ hover }">
            <v-card
              :elevation="hover ? 12 : 2"
              :class="{ 'on-hover': hover }"
            >
              <v-img
                :src="item.img"
                height="225px"
              >
                  <v-row
                    class="fill-height flex-column"
                    justify="space-between"
                  >
                  
                     

                  </v-row>
              
              </v-img>
              <b-button  block href="#" v-b-toggle.accordion-2 variant="info" style="background-color:#d9a4f5">See more info</b-button>
                <b-collapse id="accordion-2" accordion="my-accordion" role="tabpanel">
                    <b-card-body>
                    <b-card-text>{{ item.text }}</b-card-text>
                    </b-card-body>
                </b-collapse>
            </v-card>
          </v-hover>
        </v-col>
      </template>
        
    </v-row>
  </v-container>
</template>

 
<script>
  export default {
      
    data: () => ({
      icons: ['mdi-rewind', 'mdi-play', 'mdi-fast-forward'],
      items: [
      {
         
          img: 'https://i.pinimg.com/564x/e5/93/f2/e593f2b6bdf1362c6550a02d0c2b8f2c.jpg ',
          text: ' Anim pariatur cliche reprehenderit, enim eiusmod high life accusamus.',
        },
      {
         
          img: 'https://i.pinimg.com/564x/c4/e0/62/c4e06223fb8706488eee433be0c3f4a2.jpg',
          text: ' Ut non feugiat ligula. Praesent tempus eleifend dolor quis molestie. Nam euismod ex ut consectetur varius. Mauris ac est vehicula, congue sem sed, imperdiet sem.',
    
        },
        {
         
          img: 'https://i.pinimg.com/564x/b5/51/f0/b551f0b4fe364854e891bbc65089a4ee.jpg',
          text: ' Sed sit amet nulla eget nisl cursus porta. Vivamus nec vehicula turpis. ',
        },
      ],
      transparent: 'rgba(255, 255, 255, 0)',
    }),
  }

</script>

