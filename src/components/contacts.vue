<template>
  <v-container
    class="d-flex flex-column align-center justify-center"
    style="height: 100vh"
    id="contacts"
  >
    <p class="text-center text-h3 font-weight-black mb-12">Наши контакты</p>
    <p class="text-h4 mb-10">
      <strong>Тюмень, 50 лет Октября, 222 к3</strong>
    </p>
    <p class="text-h4 mb-10">
      <strong>8 3452 70 90 90 / 8 3452 700 999</strong>
    </p>
    <p class="text-h4 mb-10">
      <a href="mailto:709090@inbox.ru" class="text-black">709090@inbox.ru</a>
    </p>

    <p class="text-h4 mb-10 text-black">
      <a
        href="https://www.instagram.com/kachay_beton"
        class="text-black"
        target="_blank"
        >@kachay_beton</a
      >
    </p>
    <v-btn
      color="amber"
      @click="$emit('show-dialog')"
      size="x-large"
      class="px-12"
      >Заказать</v-btn
    >
  </v-container>
</template>
  
  <script>
export default {
  name: "Contacts",
};
</script>
  
  <style scoped>
</style>