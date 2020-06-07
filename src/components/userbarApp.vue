<template>
  <div class="text-center">
    <v-menu offset-y>
      <template v-slot:activator="{ on }">
        <v-btn
          class="blue lighten-1"
          v-on="on"
        >
          <v-icon color="white">mdi-account-outline</v-icon>
        </v-btn>
      </template>
      <v-list>
        <v-list-item justify="center">
            <v-list-item-avatar>
                <v-icon>mdi-account-check</v-icon>
            </v-list-item-avatar>
            <v-list-item-content class="name">Иванов Иван</v-list-item-content>
        </v-list-item>
        <v-list-item
          v-for="(item, index) in items"
          :key="index"
          class="text-center"
        >

          <v-list-item-title href="#">{{ item.title }}</v-list-item-title>
        </v-list-item>
      </v-list>
    </v-menu>
  </div>
</template>

<script>
  export default {
    
    data: () => ({
      user: [
          { pic: '/img/user/logo.png', name: 'Ivan Ivanov'}
      ],
      items: [
        { title: 'Профиль' },
        { title: 'Выйти' },
      ],
    }),
  }
</script>