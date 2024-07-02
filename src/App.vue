<template>
  <v-app>
    <Header />
    <v-main>
      <HeroSection @show-dialog="showDialog" />
      <ServicesGallery @show-dialog="showDialog" />
      <Gallery />
      <Partners />
      <Contacts @show-dialog="showDialog" />
    </v-main>
  </v-app>
  <v-dialog v-model="dialog" max-width="500px">
    <v-card class="d-flex">
      <v-card-title>Выберите опцию заказа</v-card-title>
      <v-card-text class="justify-center">
        <v-btn block color="amber" @click="call" class="mb-6"
          >Звонок 70-90-90</v-btn
        >
        <v-btn block color="amber" @click="email">Почта 709090@inbox.ru</v-btn>
      </v-card-text>
      <v-card-actions>
        <v-btn @click="dialog = false">Отмена</v-btn>
      </v-card-actions>
    </v-card>
  </v-dialog>
</template>

<script>
import Header from "./components/header/header.vue";
import HeroSection from "./components/header/hero_section.vue";
import ServicesGallery from "./components/equipment/services_gallery.vue";
import Gallery from "./components/gallery/gallery.vue";
import Partners from "./components/partners.vue";
import Contacts from "./components/contacts.vue";
//
// import OrderDialog from "./components/order_dialog.vue";

export default {
  name: "App",
  components: {
    Header,
    HeroSection,
    ServicesGallery,
    Gallery,
    Partners,
    Contacts,
    // OrderDialog,
  },
  data() {
    return {
      dialog: false,
    };
  },
  methods: {
    showDialog() {
      this.dialog = true;
    },
    call() {
      window.open("tel:+73452709090");
      this.dialog = false;
    },
    email() {
      window.open("mailto:709090@inbox.ru");
      this.dialog = false;
    },
  },
};
</script>

<style>
.price {
  display: flex;
  align-items: baseline;
}
.small {
  font-size: 0.75rem;
  margin-right: 4px;
}
.big {
  font-size: 1.5rem;
  margin-right: 4px;
}
.currency {
  font-size: 0.875rem;
}
</style>