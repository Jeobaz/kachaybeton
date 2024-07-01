<template>
  <v-container class="bg" fluid>
    <v-row class="d-flex">
      <v-col cols="12" md="6" class="center ml-sm-0 mt-md-12 ml-0">
        <v-col cols="12" class="ml-sm-0 ml-md-12 mb-6">
          <p class="text-md-h4 font-weight-black text-h6">
            Продажа бетона любой марки
          </p>
        </v-col>
        <v-col cols="12" class="ml-sm-0 ml-md-12 mb-6">
          <p class="text-md-h4 font-weight-black text-h6">
            Услуги автобетоносмесителей, автобетононасосов
          </p>
        </v-col>
        <v-col cols="12" class="ml-sm-0 ml-md-12 mb-6">
          <p class="text-md-h4 font-weight-black text-h6">
            Работаем на территории Тюмени и Тюменской области
          </p>
        </v-col>
        <v-col cols="12" class="ml-sm-0 ml-md-12 mb-6">
          <p class="text-md-h4 font-weight-black text-h6">
            Гибкие условия аренды.
          </p>
        </v-col>
        <v-col
          cols="12"
          class="d-flex ml-sm-0 ml-md-12 justify-center justify-md-start"
        >
          <v-btn color="amber" @click="showOrderDialog" size="x-large"
            >Заказать</v-btn
          >
        </v-col>
      </v-col>

      <v-col cols="12" md="6" class="d-none d-md-flex">
        <v-img src="/src/assets/hero/hero.png" alt="Автобетононасос"></v-img>
      </v-col>
    </v-row>
    <v-dialog v-model="dialog" max-width="500px">
      <v-card class="d-flex">
        <v-card-title>Выберите опцию заказа</v-card-title>
        <v-card-text class="justify-center">
          <v-btn block color="amber" @click="call" class="mb-6"
            >Звонок +7 999 999 99 99</v-btn
          >

          <v-btn block color="amber" @click="email">Почта test@test.ru</v-btn>
        </v-card-text>
        <v-card-actions>
          <v-btn @click="dialog = false">Отмена</v-btn>
        </v-card-actions>
      </v-card>
    </v-dialog>
  </v-container>
</template>
  
  <script>
export default {
  name: "HeroSection",
  data() {
    return {
      dialog: false,
      selectedOption: "",
    };
  },
  props: {
    callPhone: {
      type: Function,
      required: true,
    },
    typeEmail: {
      type: Function,
      required: true,
    },
  },
  methods: {
    showOrderDialog() {
      this.dialog = true;
    },
    call() {
      window.open("tel:+79999999999");
      this.dialog = false;
    },
    email() {
      window.open("mailto:test@test.ru");
      this.dialog = false;
    },
  },
};
</script>
  

<style scoped>
.bg {
  background: url("src/assets/hero/bg.png");
  background-size: cover;
}
</style>