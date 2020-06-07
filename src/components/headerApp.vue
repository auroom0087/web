
<template>

  <v-card
    color="grey lighten-4"
    tile
  >
  <v-container >

    <v-toolbar flat color="grey lighten-4">
      <v-row justify="center">
        <v-toolbar-title class="mr-3 pl-2 pr-2" height="36px" >iАлтай</v-toolbar-title>
        <div height="36px">
          <v-toolbar-items-group v-model="item" >
            <v-btn 
              v-for="(item, index) in items"
              :key="index"
              :href="item.href"
              class="pa-2"
              text
              >
              <span> {{ item.title }} </span>
            </v-btn>
          </v-toolbar-items-group>

        </div> 
        <v-spacer></v-spacer>

        <v-card>
          <userbarApp/>
        </v-card>

        
      </v-row>
      
    </v-toolbar>
  
  </v-container>
    

    
  </v-card>
</template>


<script>
import userbarApp from './userbarApp'; 
   export default {
    name: 'App',

    components: {
        userbarApp
    },

    data: () => ({
        items: [
        { title: 'Голосование', icon:'mdi-vote', href:'#' },
        { title: 'Результаты', icon:'mdi-bookmark-outline', href:'#'},
        { title: 'Магазин поощрений', icon: 'mdi-cart', href:'#' },
      ]
    })
};

</script>