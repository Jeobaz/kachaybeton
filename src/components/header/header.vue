<template>
  <v-app-bar app>
    <template v-if="$vuetify.display.smAndDown">
      <v-app-bar-nav-icon
        variant="text"
        @click.stop="drawer = !drawer"
      ></v-app-bar-nav-icon>
    </template>
    <v-row class="align-center">
      <v-img
        src="/hero/logo0.png"
        alt="Логотип"
        contain
        max-height="40"
        max-width="200"
      ></v-img>
      <p class="text-h6 black--text">КачайБетон</p>
    </v-row>

    <template v-if="$vuetify.display.mdAndUp">
      <v-spacer></v-spacer>

      <v-btn
        v-for="item in items"
        :key="item.value"
        @click="scrollTo(item.value)"
      >
        {{ item.title }}
      </v-btn>
    </template>
  </v-app-bar>

  <v-navigation-drawer
    v-model="drawer"
    :location="$vuetify.display.mobile ? 'bottom' : undefined"
    temporary
  >
    <v-list>
      <v-list-item
        v-for="item in items"
        :key="item.value"
        @click="onBottomSheetClick(item.value)"
      >
        <v-list-item-content>
          <p @click="scrollTo(item.value)">{{ item.title }}</p>
        </v-list-item-content>
      </v-list-item>
    </v-list>
  </v-navigation-drawer>
</template>
  
  <script>
export default {
  name: "Header",
  methods: {
    onBottomSheetClick(id) {
      this.drawer = false;
      scrollTo(id);
    },
    scrollTo(id) {
      const element = document.getElementById(id);
      if (element) {
        element.scrollIntoView({ behavior: "smooth" });
      }
    },
  },
  data: () => ({
    drawer: false,
    group: null,
    items: [
      {
        title: "Услуги",
        value: "services",
      },
      {
        title: "Работы",
        value: "gallery",
      },
      {
        title: "Клиенты",
        value: "partners",
      },
      {
        title: "Контакты",
        value: "contacts",
      },
    ],
  }),

  watch: {
    group() {
      this.drawer = false;
    },
  },
};
</script>

<style scoped>
.ml-3 {
  margin-left: 16px;
}
</style>
  