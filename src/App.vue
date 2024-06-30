<template>
  <v-app>
    <Header />
    <v-main>
    <HeroSection fill-height :callPhone="call" :typeEmail="email"/>
    <h1 class="text-center pb-4" id="services">Наша техника</h1>
    <v-container fill-height id="service">
      <v-row>
      
        <v-col cols="12">
          <v-row>
           
            <EquipmentCard
              v-for="equipment in equipmentList"
              :key="equipment.id"
              :equipment="equipment"
            />
            <TableCard />
          </v-row>
         
            
            
        </v-col>
      </v-row>
    </v-container>   

    <Gallery />
    <Partners />
   
    
  </v-main>
  </v-app>
</template>

<script>
import EquipmentCard from "./components/cards.vue";
import HeroSection from "./components/hero_section.vue";
import Gallery from "./components/gallery.vue";
import TableCard from "./components/table_card.vue";
import Partners from "./components/partners.vue";


export default {
  name: "App",
  components: {
    EquipmentCard,
    HeroSection,
    Gallery,
    TableCard,
    Partners
  
  },
  methods:{
    methods: {
    dialog() {
      this.dialog = true;
    },
    call(){ 
      window.open('tel:+79999999999');
      // window.location.href = 'tel:+79999999999';
      // this.dialog = false;
    },
    email() {
      window.open("mailto:test@test.ru");
      // window.location.href = 'mailto:test@test.ru';
      // this.dialog = false;
    }
  }
  },
  data() {
    return {
      equipmentList: [
        {
          id: 1,
          title: 'Автобетоносмеситель',
          price: '350',
          priceFrom: true,
          description1: 'В наличии 8 единиц техники',
          description2: 'Доступные объемы от 9 до 16м³',
          caption: 'Минимальный объем 7 м³',

          path: "src/assets/cards/mixer.png",
        },
        {
          id: 2,
          title: 'Автобетононасос',
          price: '300',
          priceFrom: false,
          description1: 'Высота подачи 47 и 57м',
          description2: 'Размер площадки 7 х 9м',
          caption: 'Минимальный объем 50 м³ / 15 000₽',
          path: "src/assets/cards/pump.png",
        },
        {
          id: 3,
          title: 'Автобетононасос с бетоносмесителем',
          price: '300',
          priceFrom: true,
          description1: 'Высота подачи до 25м',
          description2: 'Размер площадки 4 х 5м',
          caption:'Минимальный объем 40 м³ / 12 000₽',
          path: "src/assets/cards/mixer.png",
        },
        {
          id: 4,
          title: 'Автобетононасос с бетоносмесителем',
          price: '300',
          priceFrom: false,
          description1: 'Высота подачи 47 и 57м',
          description2: 'Размер площадки 7 х 9м',
          path: "src/assets/cards/pump_with_mixer.png",
        },
        {
          id: 5,
          title: 'Насос стационарный',
          price: '350',
          priceFrom: true,
          description1: 'Высота подачи 47 и 57м',
          description2: 'Размер площадки 7 х 9м',
          path: "src/assets/cards/pump_static.png",
        },
      ],
    };
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