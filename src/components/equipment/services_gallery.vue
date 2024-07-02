<template>
  <v-container class="mt-12">
    <v-container style="height: 100vh" class="mb-12">
      <p class="text-center text-h3 font-weight-black" id="services">
        Товарный бетон
      </p>
      <TableCard @show-dialog="$emit('show-dialog')" />
    </v-container>
    <v-container fill-height id="service">
      <p class="text-center text-h3 font-weight-black mb-12">Наша техника</p>
      <v-row>
        <v-col cols="12">
          <v-row class="d-flex flex-row align-stretch">
            <EquipmentCards
              v-for="equipment in equipmentList"
              :key="equipment.id"
              :equipment="equipment"
              @show-dialog="$emit('show-dialog')"
            />
          </v-row>
        </v-col>
      </v-row> </v-container
  ></v-container>
</template>

<script>
import EquipmentCards from "./equipment_cards.vue";
import TableCard from "./table_card.vue";

export default {
  name: "ServicesGallery",
  components: { EquipmentCards, TableCard },
  props: {
    equipment: {
      type: Object,
      required: true,
    },
  },

  data() {
    return {
      equipmentList: [
        {
          id: 1,
          title: "Автобетоносмеситель",
          price: "600",
          useBasePriceCaption: true,
          priceFrom: true,
          description1: "В наличии 8 единиц техники",
          description2: "Доступные объемы от 9 до 16м³",
          caption: "Минимальный объем 7 м³",

          path: "/cards/mixer.png",
        },
        {
          id: 2,
          title: "Автобетононасос",
          price: "500",
          useBasePriceCaption: true,
          priceFrom: false,
          description1: "Высота подачи 47 и 57м",
          description2: "Размер площадки 7 х 9м",
          caption: "Минимальный объем 50 м³ / 18 000₽",
          path: "/cards/pump.png",
        },
        {
          id: 4,
          title: "Автобетононасос \n с бетоносмесителем",
          price: "20 000",
          priceCaption: "/ рейс",
          useBasePriceCaption: false,
          priceFrom: false,
          description1: "Высота подачи до 25м",
          description2: "Размер площадки 4 х 5м",
          caption: "",
          path: "/cards/pump_with_mixer.png",
        },
      ],
    };
  },
};
</script>