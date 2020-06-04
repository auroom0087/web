<template>
  <v-app>
   
    <v-content>
      <HelloWorld/>
      <loginApp />
    </v-content>
  </v-app>
</template>

<script>
import HelloWorld from './components/HelloWorld';
import loginApp from './components/loginApp';

export default {
  name: 'App',

  components: {
    HelloWorld,
    loginApp
  },

  data: () => ({
    //
  }),
};
</script>
