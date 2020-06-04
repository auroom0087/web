
<template>
  <v-card
    color="grey lighten-4"
    tile
  >
    <v-toolbar flat extended>

      <v-toolbar-title>ЕРА ГОЛОСУЕТ </v-toolbar-title>

      <v-spacer></v-spacer>

      <v-btn icon>
        <v-icon>mdi-heart</v-icon>
      </v-btn>

      <loginApp />
    </v-toolbar>
  </v-card>
</template>

<script>
import loginApp from './loginApp'; 
   export default {
    name: 'App',

    components: {
        loginApp
    },

    data: () => ({
        //
    }),
};

</script>