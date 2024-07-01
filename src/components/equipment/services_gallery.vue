<template>
  <p class="text-center text-h3 font-weight-black mb-12" id="services">
    Товарный бетон
  </p>
  <v-container fill-height id="service">
    <TableCard />
    <p class="text-center text-h3 font-weight-black mb-12">Наша техника</p>
    <v-row>
      <v-col cols="12">
        <v-row>
          <EquipmentCards
            v-for="equipment in equipmentList"
            :key="equipment.id"
            :equipment="equipment"
          />
        </v-row>
      </v-col>
    </v-row>
  </v-container>
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
          price: "350",
          priceFrom: true,
          description1: "В наличии 8 единиц техники",
          description2: "Доступные объемы от 9 до 16м³",
          caption: "Минимальный объем 7 м³",

          path: "src/assets/cards/mixer.png",
        },
        {
          id: 2,
          title: "Автобетононасос",
          price: "300",
          priceFrom: false,
          description1: "Высота подачи 47 и 57м",
          description2: "Размер площадки 7 х 9м",
          caption: "Минимальный объем 50 м³ / 15 000₽",
          path: "src/assets/cards/pump.png",
        },
        {
          id: 3,
          title: "Автобетононасос с бетоносмесителем",
          price: "300",
          priceFrom: true,
          description1: "Высота подачи до 25м",
          description2: "Размер площадки 4 х 5м",
          caption: "Минимальный объем 40 м³ / 12 000₽",
          path: "src/assets/cards/mixer.png",
        },
        {
          id: 4,
          title: "Автобетононасос с бетоносмесителем",
          price: "300",
          priceFrom: false,
          description1: "Высота подачи 47 и 57м",
          description2: "Размер площадки 7 х 9м",
          path: "src/assets/cards/pump_with_mixer.png",
        },
        {
          id: 5,
          title: "Насос стационарный",
          price: "350",
          priceFrom: true,
          description1: "Высота подачи 47 и 57м",
          description2: "Размер площадки 7 х 9м",
          path: "src/assets/cards/pump_static.png",
        },
      ],
    };
  },
};
</script>