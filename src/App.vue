<template>
  <v-app>
   
    <v-content >
      <HelloWorld/>
      <headerApp />
    </v-content>
  </v-app>
</template>

<script>
import HelloWorld from './components/HelloWorld';
import headerApp from './components/headerApp';


export default {
  name: 'App',

  components: {
    HelloWorld,
    headerApp
  },

  data: () => ({
    //
  }),
};
</script>
