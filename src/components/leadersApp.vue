<template>
    <v-card class="pa-3">
        <h2>Лидеры мнений</h2>
        <v-row justify="center">
            <v-col cols="12"
            sm="4" 
            md="3"
            v-for="(user, index) in users"
            :key="index">
                <v-card
                    class="mx-auto"
                >
                    <v-list-item>
                    <v-list-item-avatar color="grey">
                        <v-img :src="user.pic"></v-img>
                    </v-list-item-avatar>
                    <v-list-item-content>
                        <v-list-item-title class="headline">{{user.name}}</v-list-item-title>
                    </v-list-item-content>
                    </v-list-item>

                    <v-card-text>
                        <p>{{user.about}}</p>
                        <p>Рейтинг пользователя <strong>{{ user.rate }}</strong> </p>
                    </v-card-text>

                    <v-card-actions>
                    <v-btn
                        text
                        color="primary"
                    >
                        Подписаться
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
    </v-card>
</template>

<script>
export default {
    data() {
        return {
            page: 1,
            users: [
                {name: "Петров Петр", pic: 'https://picsum.photos/350/165?random', about: `  Lorem ipsum dolor sit amet consectetur 
                dipisicing elit. Quo, numquam at. Totam, reiciendis culpa distinctio aperiam delectus, neque alias odit dolore quam, 
                accusamus dolor ea voluptatem laboriosam commodi soluta consequuntur.`, rate: "250"},
                {name: "Петров Петр", pic: 'https://picsum.photos/350/165?random', about: `  Lorem ipsum dolor sit amet consectetur 
                dipisicing elit. Quo, numquam at. Totam, reiciendis culpa distinctio aperiam delectus, neque alias odit dolore quam, 
                accusamus dolor ea voluptatem laboriosam commodi soluta consequuntur.`, rate: "250"},
                {name: "Петров Петр", pic: 'https://picsum.photos/350/165?random', about: `  Lorem ipsum dolor sit amet consectetur 
                dipisicing elit. Quo, numquam at. Totam, reiciendis culpa distinctio aperiam delectus, neque alias odit dolore quam, 
                accusamus dolor ea voluptatem laboriosam commodi soluta consequuntur.`, rate: "250"},
                {name: "Петров Петр", pic: 'https://picsum.photos/350/165?random', about: `  Lorem ipsum dolor sit amet consectetur 
                dipisicing elit. Quo, numquam at. Totam, reiciendis culpa distinctio aperiam delectus, neque alias odit dolore quam, 
                accusamus dolor ea voluptatem laboriosam commodi soluta consequuntur.`, rate: "250"},
                {name: "Петров Петр", pic: 'https://picsum.photos/350/165?random', about: `  Lorem ipsum dolor sit amet consectetur 
                dipisicing elit. Quo, numquam at. Totam, reiciendis culpa distinctio aperiam delectus, neque alias odit dolore quam, 
                accusamus dolor ea voluptatem laboriosam commodi soluta consequuntur.`, rate: "250"},
                {name: "Петров Петр", pic: 'https://picsum.photos/350/165?random', about: `  Lorem ipsum dolor sit amet consectetur 
                dipisicing elit. Quo, numquam at. Totam, reiciendis culpa distinctio aperiam delectus, neque alias odit dolore quam, 
                accusamus dolor ea voluptatem laboriosam commodi soluta consequuntur.`, rate: "250"},
                {name: "Петров Петр", pic: 'https://picsum.photos/350/165?random', about: `  Lorem ipsum dolor sit amet consectetur 
                dipisicing elit. Quo, numquam at. Totam, reiciendis culpa distinctio aperiam delectus, neque alias odit dolore quam, 
                accusamus dolor ea voluptatem laboriosam commodi soluta consequuntur.`, rate: "250"},
                {name: "Петров Петр", pic: 'https://picsum.photos/350/165?random', about: `  Lorem ipsum dolor sit amet consectetur 
                dipisicing elit. Quo, numquam at. Totam, reiciendis culpa distinctio aperiam delectus, neque alias odit dolore quam, 
                accusamus dolor ea voluptatem laboriosam commodi soluta consequuntur.`, rate: "250"},
                {name: "Петров Петр", pic: 'https://picsum.photos/350/165?random', about: `  Lorem ipsum dolor sit amet consectetur 
                dipisicing elit. Quo, numquam at. Totam, reiciendis culpa distinctio aperiam delectus, neque alias odit dolore quam, 
                accusamus dolor ea voluptatem laboriosam commodi soluta consequuntur.`, rate: "250"},
                {name: "Петров Петр", pic: 'https://picsum.photos/350/165?random', about: `  Lorem ipsum dolor sit amet consectetur 
                dipisicing elit. Quo, numquam at. Totam, reiciendis culpa distinctio aperiam delectus, neque alias odit dolore quam, 
                accusamus dolor ea voluptatem laboriosam commodi soluta consequuntur.`, rate: "250"},
                {name: "Петров Петр", pic: 'https://picsum.photos/350/165?random', about: `  Lorem ipsum dolor sit amet consectetur 
                dipisicing elit. Quo, numquam at. Totam, reiciendis culpa distinctio aperiam delectus, neque alias odit dolore quam, 
                accusamus dolor ea voluptatem laboriosam commodi soluta consequuntur.`, rate: "250"},
                {name: "Петров Петр", pic: 'https://picsum.photos/350/165?random', about: `  Lorem ipsum dolor sit amet consectetur 
                dipisicing elit. Quo, numquam at. Totam, reiciendis culpa distinctio aperiam delectus, neque alias odit dolore quam, 
                accusamus dolor ea voluptatem laboriosam commodi soluta consequuntur.`, rate: "250"},
            ]
        }
    }
}
</script>
