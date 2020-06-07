<template>
  <v-app>
   
    <v-content >
      <headerApp />
      <v-container>
        <shopApp/>
      </v-container> 
      <footerApp class="mt-5"/>
    </v-content>
  </v-app>
</template>



<script>
import headerApp from './components/headerApp';
import footerApp from './components/footerApp';
import shopApp from './components/shopApp';

export default {
  name: 'App',

  components: {
    headerApp,
    footerApp,
    shopApp
  },

  data: () => ({
    //
  }),
};
</script>
