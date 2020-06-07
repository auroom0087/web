<template>
  <v-footer
    padless
    class="blue darken-1"
  >
  <v-container>
    <v-card
        flat
        class="blue darken-1 flex"
        >
        <v-card-title>
            <v-card>
                <v-btn v-for="(item, index) in menu"
                :key="index"
                :href="item.href"
                text
                >
                    <span>{{item.name}}</span>
                </v-btn>
            </v-card>

            <v-spacer></v-spacer>

            <v-btn
            v-for="icon in icons"
            :key="icon"
            class="mx-4"
            dark
            icon
            href="#"
            >
            <v-icon size="24px">{{ icon }}</v-icon>
            </v-btn>
        </v-card-title>

        <v-card-text class="py-2 white--text text-center">
            {{ new Date().getFullYear() }} — <strong>iАлтай</strong>
        </v-card-text>
        </v-card>
  </v-container>
    
  </v-footer>
</template>

<script>
  export default {
    data: () => ({
      icons: [
        'mdi-telegram',
        'mdi-twitter',
        'mdi-vk',
        'mdi-instagram',
      ],
      menu: [
          {name: 'Голосование', href: '#', },
          {name: 'Результаты', href: '#', },
          {name: 'Магазин поощрений', href: '#', },
          {name: 'О проекте', href: '#', },
          
      ]
    }),
  }
</script>