<template>
  <div>
    <v-btn color="amber" @click="showDialog" size="x-large">Заказать</v-btn>
    <v-dialog v-model="dialog" max-width="500px">
      <v-card class="d-flex">
        <v-card-title>Выберите опцию заказа</v-card-title>
        <v-card-text class="justify-center">
          <v-btn block color="amber" @click="call" class="mb-6"
            >Звонок 70-90-90</v-btn
          >
          <v-btn block color="amber" @click="email"
            >Почта 709090@inbox.ru</v-btn
          >
        </v-card-text>
        <v-card-actions>
          <v-btn @click="dialog = false">Отмена</v-btn>
        </v-card-actions>
      </v-card>
    </v-dialog>
  </div>
</template>
  
  <script>
export default {
  name: "OrderDialog",
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
      window.open("tel:709090");
      this.dialog = false;
    },
    email() {
      window.open("mailto:709090@inbox.ru");
      this.dialog = false;
    },
  },
};
</script>
  
  <style scoped>
/* ваши стили */
</style>