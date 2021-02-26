<template>
  <img ref="responsive-image" :src="images[0].path" :alt="alt" />
</template>

<script>
export default {
  props: ["images", "alt"],
  mounted() {
    console.log(this.images);
    var el = this.$refs["responsive-image"];
    this.images.forEach((image) => {
      if (window.matchMedia("(min-width: " + image.width + "px)").matches) {
        console.log("LOAD", image.path);
        el.src = image.path;
      }
    });
  },
};
</script>