<template>
  <v-container id="partners">
    <p class="text-center text-h3 font-weight-black mb-12">Наши партнеры</p>
    <v-card class="partners-card">
      <v-row justify="space-around">
        <v-col
          v-for="(partner, index) in partners"
          :key="index"
          cols="6"
          sm="4"
          md="2"
          class="partner-col"
        >
          <v-img :src="partner.src" :alt="partner.name" contain cover></v-img>
        </v-col>
      </v-row>
    </v-card>
  </v-container>
</template>
  
  <script>
export default {
  name: "Parnters",
  data() {
    return {
      partners: [
        { name: "СБК", src: "src/assets/logos/sbk.png" },
        { name: "Звезда", src: "src/assets/logos/zvezda.png" },
        { name: "Евробетон", src: "src/assets/logos/evrobeton.png" },
        { name: "БСС", src: "src/assets/logos/bss.png" },
        { name: "Темпстрой", src: "src/assets/logos/tempstroy.png" },
        { name: "Строй Капитал", src: "src/assets/logos/sk.png" },
      ],
    };
  },
};
</script>
  
  <style scoped>
.partners-card {
  background-color: #e0e0e0;
  border-radius: 8px;
  padding: 16px;
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
}
/* .partner-col {
    max-width: 200px;
  } */
.text-center {
  text-align: center;
}
</style>
  