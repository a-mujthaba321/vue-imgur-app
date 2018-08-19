<template>
  <div>
    <img v-for="image in allImages" :key="image.link" :src="image.link" width="300">
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

<style>
</style>
