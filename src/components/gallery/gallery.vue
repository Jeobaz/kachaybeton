<template>
  <v-container id="gallery">
    <p class="text-center text-h3 font-weight-black mb-12">Наши работы</p>

    <v-row>
      <GalleryCard v-for="image in images" :key="image.id" :image="image" />
    </v-row>
  </v-container>
</template>

  
  
  <script>
import GalleryCard from "./gallery_card.vue";

export default {
  name: "Gallery",
  components: {
    GalleryCard,
  },

  data() {
    return {
      images: [
        {
          id: 1,
          src: "src/assets/gallery/slide1.webp",
        },
        {
          id: 2,
          src: "src/assets/gallery/slide2.webp",
        },
        {
          id: 3,
          src: "src/assets/gallery/slide3.webp",
        },
        {
          id: 4,
          src: "src/assets/gallery/slide4.webp",
        },
        {
          id: 5,
          src: "src/assets/gallery/slide5.webp",
        },
        {
          id: 6,
          src: "src/assets/gallery/slide6.webp",
        },
      ],
    };
  },
};
</script>
  
  <style scoped>
.gallery-card {
  height: 300px;
  background-color: #f0f0f0; /* Grey background */
  overflow: hidden;
}
</style>