<template>
  <v-app>
    <Header />
    <v-main>
      <HeroSection fill-height :callPhone="call" :typeEmail="email" />
      <ServicesGallery />
      <Gallery />
      <Partners />
      <Contacts />
    </v-main>
  </v-app>
</template>

<script>
import Header from "./components/header/header.vue";
import HeroSection from "./components/header/hero_section.vue";
import ServicesGallery from "./components/equipment/services_gallery.vue";
import Gallery from "./components/gallery/gallery.vue";
import Partners from "./components/partners.vue";
import Contacts from "./components/contacts.vue";

export default {
  name: "App",
  components: {
    Header,
    HeroSection,
    ServicesGallery,
    Gallery,
    Partners,
    Contacts,
  },
  methods: {
    methods: {
      dialog() {
        this.dialog = true;
      },
      call() {
        window.open("tel:+79999999999");
        // window.location.href = 'tel:+79999999999';
        // this.dialog = false;
      },
      email() {
        window.open("mailto:test@test.ru");
        // window.location.href = 'mailto:test@test.ru';
        // this.dialog = false;
      },
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