<template>
     <v-col cols="12" sm="6" md="4">
          <v-card class="gallery-card">
            <v-img
              :src="image.src"
              aspect-ratio="3/2"
              contain
              gradient="to bottom, rgba(0,0,0,.1), rgba(0,0,0,.5)"
              cover
            ></v-img>
          </v-card>
        </v-col>
</template>

<script>
export default {
  name: "GalleryCard",
  props: {
    image: {
      type: Object,
      required: true,
    },
  },
};
</script>

