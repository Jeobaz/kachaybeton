<template fill-height>
  <v-container class="bg px-0" fluid>
    <v-row class="d-flex align-center" style="height: 100vh">
      <v-col cols="12" md="6" class="ml-sm-0 ml-0">
        <MobileHeader v-if="$vuetify.display.smAndDown" />
        <v-col
          cols="12"
          class="ml-sm-0 ml-md-12 mb-6"
          v-if="$vuetify.display.mdAndUp"
        >
          <p class="text-md-h3 font-weight-black text-h5">
            Компания «КачайБетон»
          </p>
        </v-col>
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
          <v-btn color="amber" @click="$emit('show-dialog')" size="x-large"
            >Заказать</v-btn
          >
        </v-col>
      </v-col>

      <v-col cols="12" md="6" class="d-none d-md-flex pump pa-0">
        <v-img src="/hero/hero.png" alt="Автобетононасос" cover></v-img>
      </v-col>
    </v-row>
  </v-container>
</template>
  
  <script>
import MobileHeader from "./mobile_header.vue";
export default {
  name: "HeroSection",
  components: { MobileHeader },
};
</script>
  

<style scoped>
.bg {
  background: url("/hero/bg.png");
  background-size: cover;
  height: 100vh;
}
.pump {
  height: 100vh;
}
</style>