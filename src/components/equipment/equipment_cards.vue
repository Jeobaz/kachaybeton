<template>
  <v-col cols="xs-1">
    <v-card class="d-flex flex-column" height="100%">
      <v-card-title class="headline">{{ equipment.title }}</v-card-title>
      <v-divider></v-divider>
      <v-card-title class="price">
        <span v-if="equipment.priceFrom" class="small text-h6 black--text"
          >от</span
        >
        <span class="big text-h4 font-weight-black">{{ equipment.price }}</span>

        <span v-if="equipment.useBasePriceCaption" class="currency text-h6"
          >₽ / м³</span
        >
        <span v-else>{{ equipment.priceCaption }}</span>
      </v-card-title>
      <v-card-text class="flex">
        <p>{{ equipment.description1 }}</p>
        <p>{{ equipment.description2 }}</p>
        <p class="mt-3 text-subtitle-2 black--text">{{ equipment.caption }}</p>
      </v-card-text>
      <v-img
        :src="equipment.path"
        class="white--text"
        max-height="200px"
        contain
        cover
      ></v-img>

      <v-divider></v-divider>
      <v-card-actions>
        <v-btn
          color="amber darke2-3"
          block
          varitant="tonal"
          @click="$emit('show-dialog')"
          >Заказать</v-btn
        >
      </v-card-actions>
    </v-card>
  </v-col>
</template>
  
  <script>
export default {
  name: "EquipmentCards",
  components: {},
  props: {
    equipment: {
      type: Object,
      required: true,
    },
  },
};
</script>

<style>
.price {
  display: flex;
  align-items: baseline;
}
</style>