<template>
    <div>
        <v-row justify="center">
            <v-col cols="3"
            v-for="(vote, index) in votes"
                :key="index">
                <v-card
                    class="mx-auto"
                    max-width="400"
                    
                    cols='3'
                >
                    <v-img
                    class="white--text align-end"
                    height="200px"
                    :src="vote.pic"
                    >
                    <v-card-title>{{vote.name}}</v-card-title>
                    </v-img>

                    <v-card-text class="text--primary">
                    <div>{{vote.prew}}</div>
                    <div><strong>За голосование Вы получите +{{ vote.rate }} баллов</strong></div>
                    </v-card-text>

                    <v-card-actions>
                    <v-btn
                        color="blue"
                        text
                    >
                        Голосовать
                    </v-btn>

                    </v-card-actions>
                </v-card>
            </v-col>
        </v-row>
        <v-btn href="#" class="d-block pa-2" color="primary">Больше голосований</v-btn>
    </div>
</template>

<script>
export default {
    data: () => ({
        votes :[
            {name: 'Название голосование', pic: 'https://avatars.mds.yandex.net/get-zen_doc/1657335/pub_5d33cf0414f98000adeae2dd_5d33d0cbc31e4900ad7fdddc/scale_1200', prew: 'sreihg;oaiprgjk;paweriooooogvjkpaiorgjk;reajowegvko', rate: '20'},
            {name: 'Название голосование', pic: 'https://avatars.mds.yandex.net/get-zen_doc/1657335/pub_5d33cf0414f98000adeae2dd_5d33d0cbc31e4900ad7fdddc/scale_1200', prew: 'sreihg;oaiprgjk;paweriooooogvjkpaiorgjk;reajowegvko', rate: '20'},
            {name: 'Название голосование', pic: 'https://avatars.mds.yandex.net/get-zen_doc/1657335/pub_5d33cf0414f98000adeae2dd_5d33d0cbc31e4900ad7fdddc/scale_1200', prew: 'sreihg;oaiprgjk;paweriooooogvjkpaiorgjk;reajowegvko', rate: '20'},
            {name: 'Название голосование', pic: 'https://avatars.mds.yandex.net/get-zen_doc/1657335/pub_5d33cf0414f98000adeae2dd_5d33d0cbc31e4900ad7fdddc/scale_1200', prew: 'sreihg;oaiprgjk;paweriooooogvjkpaiorgjk;reajowegvko', rate: '20'},

        ]
    }),
};
</script>