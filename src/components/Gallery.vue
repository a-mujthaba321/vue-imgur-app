<template>
  <div class="image-container">
    <img v-for="image in allImages" :key="image.link" :src="image.link">
  </div>
</template>

<script>
import { mapActions, mapGetters } from "vuex";
export default {
  name: "Gallery",
  computed: mapGetters(["allImages"]),
  created() {
    this.fetchImages();
  },
  methods: mapActions(["fetchImages"])
};
</script>

<style scoped>
.image-container {
  column-count: 2;
  column-gap: 0;
}

.img {
  max-width: 100%;
  padding: 5px;
}
</style>
