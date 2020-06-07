<template>
    <div class="pa-3">
       <h2>Магазин поощрений</h2>
       <v-row justify="center">
           <v-col cols="12" xs="6" md="3"
            v-for="(item, index) in items"
                :key="index">
                <v-card
                    class="mx-auto"
                    max-width="400"
                    
                    cols='3'
                >
                    <v-img
                    class="white--text align-end"
                    height="200px"
                    :src="item.pic"
                    >
                    <v-card-title>{{item.name}}</v-card-title>
                    </v-img>

                    <v-card-text class="text--primary">
                        <div>{{item.prew}}</div>
                    </v-card-text>

                    <v-card-actions>
                    <v-btn
                        color="orange"
                        text
                    >
                        Получить
                    </v-btn>

                    </v-card-actions>
                </v-card>
           </v-col>
        </v-row>
        <div class="text-center">
            <v-pagination
            v-model="page"
            :length="4"
            prev-icon="mdi-menu-left"
            next-icon="mdi-menu-right"
            ></v-pagination>
        </div> 
    </div>
</template>

<script>
export default {
    data() {
        return {
            page: 2,
            items :[
                {name: 'Билеты в кино', pic: 'https://avatars.mds.yandex.net/get-zen_doc/1657335/pub_5d33cf0414f98000adeae2dd_5d33d0cbc31e4900ad7fdddc/scale_1200', prew: `Lorem ipsum dolor sit, amet consectetur 
            adipisicing elit. Ea odit illo soluta molestiae excepturi mollitia qui eveniet porro, quam architecto dicta, quod iure adipisci omnis dolores 
            tempore animi doloribus similique`  },
                {name: 'Билеты в кино', pic: 'https://avatars.mds.yandex.net/get-zen_doc/1657335/pub_5d33cf0414f98000adeae2dd_5d33d0cbc31e4900ad7fdddc/scale_1200', prew: `Lorem ipsum dolor sit, amet consectetur 
            adipisicing elit. Ea odit illo soluta molestiae excepturi mollitia qui eveniet porro, quam architecto dicta, quod iure adipisci omnis dolores 
            tempore animi doloribus similique`  },
                {name: 'Билеты в кино', pic: 'https://avatars.mds.yandex.net/get-zen_doc/1657335/pub_5d33cf0414f98000adeae2dd_5d33d0cbc31e4900ad7fdddc/scale_1200', prew: `Lorem ipsum dolor sit, amet consectetur 
            adipisicing elit. Ea odit illo soluta molestiae excepturi mollitia qui eveniet porro, quam architecto dicta, quod iure adipisci omnis dolores 
            tempore animi doloribus similique`  },
                {name: 'Билеты в кино', pic: 'https://avatars.mds.yandex.net/get-zen_doc/1657335/pub_5d33cf0414f98000adeae2dd_5d33d0cbc31e4900ad7fdddc/scale_1200', prew: `Lorem ipsum dolor sit, amet consectetur 
            adipisicing elit. Ea odit illo soluta molestiae excepturi mollitia qui eveniet porro, quam architecto dicta, quod iure adipisci omnis dolores 
            tempore animi doloribus similique`  },
            {name: 'Билеты в кино', pic: 'https://avatars.mds.yandex.net/get-zen_doc/1657335/pub_5d33cf0414f98000adeae2dd_5d33d0cbc31e4900ad7fdddc/scale_1200', prew: `Lorem ipsum dolor sit, amet consectetur 
            adipisicing elit. Ea odit illo soluta molestiae excepturi mollitia qui eveniet porro, quam architecto dicta, quod iure adipisci omnis dolores 
            tempore animi doloribus similique`  },
                {name: 'Билеты в кино', pic: 'https://avatars.mds.yandex.net/get-zen_doc/1657335/pub_5d33cf0414f98000adeae2dd_5d33d0cbc31e4900ad7fdddc/scale_1200', prew: `Lorem ipsum dolor sit, amet consectetur 
            adipisicing elit. Ea odit illo soluta molestiae excepturi mollitia qui eveniet porro, quam architecto dicta, quod iure adipisci omnis dolores 
            tempore animi doloribus similique`  },
                {name: 'Билеты в кино', pic: 'https://avatars.mds.yandex.net/get-zen_doc/1657335/pub_5d33cf0414f98000adeae2dd_5d33d0cbc31e4900ad7fdddc/scale_1200', prew: `Lorem ipsum dolor sit, amet consectetur 
            adipisicing elit. Ea odit illo soluta molestiae excepturi mollitia qui eveniet porro, quam architecto dicta, quod iure adipisci omnis dolores 
            tempore animi doloribus similique`  },
                {name: 'Билеты в кино', pic: 'https://avatars.mds.yandex.net/get-zen_doc/1657335/pub_5d33cf0414f98000adeae2dd_5d33d0cbc31e4900ad7fdddc/scale_1200', prew: `Lorem ipsum dolor sit, amet consectetur 
            adipisicing elit. Ea odit illo soluta molestiae excepturi mollitia qui eveniet porro, quam architecto dicta, quod iure adipisci omnis dolores 
            tempore animi doloribus similique`  },
            {name: 'Билеты в кино', pic: 'https://avatars.mds.yandex.net/get-zen_doc/1657335/pub_5d33cf0414f98000adeae2dd_5d33d0cbc31e4900ad7fdddc/scale_1200', prew: `Lorem ipsum dolor sit, amet consectetur 
            adipisicing elit. Ea odit illo soluta molestiae excepturi mollitia qui eveniet porro, quam architecto dicta, quod iure adipisci omnis dolores 
            tempore animi doloribus similique`  },
                {name: 'Билеты в кино', pic: 'https://avatars.mds.yandex.net/get-zen_doc/1657335/pub_5d33cf0414f98000adeae2dd_5d33d0cbc31e4900ad7fdddc/scale_1200', prew: `Lorem ipsum dolor sit, amet consectetur 
            adipisicing elit. Ea odit illo soluta molestiae excepturi mollitia qui eveniet porro, quam architecto dicta, quod iure adipisci omnis dolores 
            tempore animi doloribus similique`  },
                {name: 'Билеты в кино', pic: 'https://avatars.mds.yandex.net/get-zen_doc/1657335/pub_5d33cf0414f98000adeae2dd_5d33d0cbc31e4900ad7fdddc/scale_1200', prew: `Lorem ipsum dolor sit, amet consectetur 
            adipisicing elit. Ea odit illo soluta molestiae excepturi mollitia qui eveniet porro, quam architecto dicta, quod iure adipisci omnis dolores 
            tempore animi doloribus similique`  },
                {name: 'Билеты в кино', pic: 'https://avatars.mds.yandex.net/get-zen_doc/1657335/pub_5d33cf0414f98000adeae2dd_5d33d0cbc31e4900ad7fdddc/scale_1200', prew: `Lorem ipsum dolor sit, amet consectetur 
            adipisicing elit. Ea odit illo soluta molestiae excepturi mollitia qui eveniet porro, quam architecto dicta, quod iure adipisci omnis dolores 
            tempore animi doloribus similique`  },
            ],
        }
    }
};
</script>