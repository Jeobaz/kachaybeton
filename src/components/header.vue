<template>
    <v-app-bar app>
      <v-row class="d-none d-md-flex">
      <span class="text-h6 ml-12 ">КачайБетон</span>
       <v-img src="/src/assets/hero/logo0.png" alt="Логотип" contain max-height="40" max-width='200'></v-img>
     </v-row>
    
      <v-spacer></v-spacer>
      <v-btn text @click="scrollTo('services')">Услуги</v-btn>
      <v-btn text @click="scrollTo('gallery')">Работы</v-btn>
      <v-btn text @click="scrollTo('contacts')">Контакты</v-btn>
    </v-app-bar>
  </template>
  
  <script>
  export default {
    name: "Header",
    methods: {
      scrollTo(id) {
        const element = document.getElementById(id);
        if (element) {
          element.scrollIntoView({ behavior: 'smooth' });
        }
      }
    }
  };
  </script>

<style scoped>
.ml-3 {
  margin-left: 16px;
}
</style>
  