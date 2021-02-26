<template>
  <div class="anim-scale">
    <ResponsiveImage
      :key="0"
      :class="[index == 0 ? 'opacity-100' : 'opacity-0 h-0']"
      class="w-full col-span-full"
      :images="srcs[0].images"
      alt="carousel"
    />
    <ResponsiveImage
      :key="1"
      :class="[index == 1 ? 'opacity-100' : 'opacity-0 h-0']"
      class="w-full col-span-full"
      :images="srcs[1].images"
      alt="carousel"
    />
    <ResponsiveImage
      :key="2"
      :class="[index == 2 ? 'opacity-100' : 'opacity-0 h-0']"
      class="w-full col-span-full"
      :images="srcs[2].images"
      alt="carousel"
    />
    <div class="flex items-center justify-between">
      <!-- <svg
        viewBox="0 0 24 24"
        fill="none"
        stroke="currentColor"
        stroke-width="1.5"
      >
        <polyline points="15 18 9 12 15 6"></polyline>
      </svg> -->
      0{{ index + 1 }} / 0{{ srcs.length }}

      <!-- <svg
        @click="next()"
        viewBox="0 0 24 24"
        fill="none"
        stroke="currentColor"
        stroke-width="1.5"
      >
        <polyline points="9 18 15 12 9 6"></polyline>
      </svg> -->
      <arrow-button/>

    </div>
  </div>
</template>

<script>
import ArrowButton from './ArrowButton.vue';
export default {
  components: { ArrowButton },
  props: ["srcs"],
  data: () => ({
    index: 0,
  }),

  created() {
    this.index = Math.floor(Math.random() * this.srcs.length);
  },

  methods: {
    next() {
      this.index = this.index == this.srcs.length - 1 ? 0 : ++this.index;
    },
  },
};
</script>

<style lang="postcss">
svg {
  /* @apply h-8 w-8; */
}

img {
  transition: opacity 1s;
}

.anim-scale {
  transform-origin: bottom left;
  animation: 1s ease-out 0s 1 scaleIn;
}
</style>