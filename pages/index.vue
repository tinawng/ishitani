<template>
  <section class="grid grid-cols-2 gap-8">
    <div class="flex flex-col justify-center items-center">
      <h1 class="mb-2">amiisu chair</h1>
      <h3>Order No.1705</h3>
    </div>
    <div></div>
    <div class="description">
      <h3>2017</h3>
      <h3>
        <p>woods</p>
        <p>Walnut & Cherry</p>
        <p>oil-wax</p>
        <p>Lappenwachs</p>
      </h3>
    </div>
    <ResponsiveImage
      class="w-full"
      :images="img_amiisu_chair2.images"
      alt="amiisu-chair2"
    />
    <ResponsiveImage
      class="w-full col-span-full"
      :images="img_amiisu_chair3.images"
      alt="amiisu-chair3"
    />
    <Carousel :srcs="[img_amiisu_chair0, img_amiisu_chair2, img_amiisu_chair3]" />
  </section>
</template>

<script>
const img_amiisu_chair2 = require("~/assets/img/amiisu-chair2.jpg?resize&sizes[]=600&sizes[]=900&sizes[]=1200&format=webp");
const img_amiisu_chair0 = require("~/assets/img/amiisu-chair1.jpg?resize&sizes[]=1000&sizes[]=1300&sizes[]=1600&format=webp");
const img_amiisu_chair1 = require("~/assets/img/amiisu-chair1.jpg?resize&sizes[]=1000&sizes[]=1300&sizes[]=1600&format=webp");
const img_amiisu_chair3 = require("~/assets/img/amiisu-chair1.jpg?resize&sizes[]=1000&sizes[]=1300&sizes[]=1600&format=webp");
export default {
  data() {
    return {
      img_amiisu_chair2,
      img_amiisu_chair0,
      img_amiisu_chair1,
      img_amiisu_chair3,
    };
  },
};
</script>

<style lang="postcss">
section {
  @apply mx-8;
  grid-template-columns: 50% 50%;
  grid-template-rows: 28rem auto auto auto;
}

.description {
  padding-left: 50%;
}
.description h3:first-of-type {
  margin-bottom: 25%;
}
.description p:nth-of-type(2n) {
  margin-bottom: 10%;
}
</style>
