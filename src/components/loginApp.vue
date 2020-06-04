<template>
  <v-row justify="center">
    <v-dialog v-model="dialog" persistent max-width="600px">
      <template v-slot:activator="{ on }">
        <v-btn color="orange" dark v-on="on" @click="login = true">Войти</v-btn>
      </template>
      <v-card v-if="isRegister">
        <v-card-title>
          <span class="headline">Регистрация</span>
        </v-card-title>
        <v-card-text>
          <v-container>
            <v-row>
              <v-col cols="12" sm="6" md="6">
                <v-icon ><i class="fas fa-user"></i></v-icon>
                <v-text-field label="Имя*" prepend-inner-icon='mdi-account' required></v-text-field>
              </v-col>
              <v-col cols="12" sm="6" md="6">
                <v-text-field
                  label="Фамилия*"
                  prepend-inner-icon='mdi-account-outline'
                  required
                ></v-text-field>
              </v-col>
              <v-col cols="12">
                <v-text-field label="Email*"  prepend-inner-icon="mdi-email" required></v-text-field>
              </v-col>
              <v-col cols="12">
                <v-text-field label="Пароль*" :prepend-inner-icon='compareLock' type="password" required v-model="user_password1" @blur="comparePassword" :style="equalColor"></v-text-field>
              </v-col>
              <v-col cols="12">
                <v-text-field label="Повторить пароль*" :prepend-inner-icon='compareLock' type="password" required v-model="user_password2" @blur="comparePassword" :style='equalColor'></v-text-field>
              </v-col>
              <v-col cols="12">
                <v-text-field label="Номер телефона" prepend-inner-icon='mdi-phone'></v-text-field>
              </v-col>
              <v-col cols="12" sm="6" >
                <v-menu
                    ref="menu"
                    v-model="menu"
                    :close-on-content-click="false"
                    transition="scale-transition"
                    offset-y
                    min-width="290px"
                >
                    <template v-slot:activator="{ on }">
                    <v-text-field
                        v-model="date"
                        label="Дата рождения"
                        prepend-icon="mdi-calendar"
                        readonly
                        v-on="on"
                    ></v-text-field>
                    </template>
                    <v-date-picker
                    ref="picker"
                    v-model="date"
                    :max="new Date().toISOString().substr(0, 10)"
                    min="1940-01-01"
                    @change="save"
                    ></v-date-picker>
                </v-menu>
              </v-col>
              <v-col cols="12" sm="6">
                <v-autocomplete prepend-inner-icon='mdi-city'
                  :items="['Горно-Алтайск', 'Чемал', 'Майма', 'Кош-Агач', 'Турочак', 'Онугдай', 'Шебалино', 'Кызыл-Осек', 'Усть-Кокса']"
                  label="Город"
                  single-line
                ></v-autocomplete>
              </v-col>
            </v-row>
          </v-container>
          <small>*Обязательные поля</small>
        </v-card-text>
        <v-card-actions>
          <v-spacer></v-spacer>
          <v-btn color="blue darken-1" text @click="isLogin = true; isRegister = false">Войти</v-btn>
          <v-btn color="blue darken-1" text @click="dialog = false">Закрыть</v-btn>
          <v-btn color="blue darken-1" text @click="dialog = false">Зарегистрироваться</v-btn>
        </v-card-actions>
      </v-card>
      <v-card v-if="isLogin">
        <v-card-title>
            <span class="headline">Авторизация</span>
        </v-card-title>
        <v-card-text>
            <v-col cols="12">
                <v-text-field label="Email или Номер телефона" prepend-inner-icon='mdi-email' required></v-text-field>
              </v-col>
              <v-col cols="12">
                <v-text-field label="Пароль" prepend-inner-icon='mdi-lock' type="password" required></v-text-field>
              </v-col>
        </v-card-text>
        <v-card-actions>
            
            <v-spacer></v-spacer>
            <v-btn color="blue darken-1" text @click="isRegister = true; isLogin = false">Зарегистрироваться</v-btn>
            <v-btn color="blue darken-1" text @click="dialog = false">Закрыть</v-btn>
            <v-btn color="blue darken-1" text @click="dialog = false">Войти</v-btn>
        </v-card-actions>
        </v-card>
    </v-dialog>
  </v-row>
</template>


<script>
    export default {
    data() {
      return{
      dialog: false,
      isRegister: true,
      isLogin: false,
      date: null,
      menu: false, 
      user_password1: '',
      user_password2: '',
      compareLock: 'mdi-lock-open',
      equalColor:'color: black'
      }
    },
    watch: {
      menu (val) {
        val && setTimeout(() => (this.$refs.picker.activePicker = 'YEAR'))
      },
    },
    methods: {
      save (date) {
        this.$refs.menu.save(date)
      },
      comparePassword() {
        if (this.user_password1 == this.user_password2){
          this.compareLock = 'mdi-lock';
          this.equalColor = 'color: green';
        }
        else {
          this.compareLock = 'mdi-lock-open';
        }
      },
    },
  }
</script>