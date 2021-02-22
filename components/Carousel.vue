<template>
  <div class="">
    <ResponsiveImage
      class="w-full col-span-full"
      :images="srcs[index].images"
      alt="amiisu-chair-carousel"
    />
    <div class="flex items-center justify-between">
      <svg
        viewBox="0 0 24 24"
        fill="none"
        stroke="currentColor"
        stroke-width="1.5"
      >
        <polyline points="15 18 9 12 15 6"></polyline>
      </svg>
      0{{ index }} / 0{{srcs.length}}

      <svg
        @click="next()"
        viewBox="0 0 24 24"
        fill="none"
        stroke="currentColor"
        stroke-width="1.5"
      >
        <polyline points="9 18 15 12 9 6"></polyline>
      </svg>
    </div>
  </div>
</template>

<script>
export default {
  props: ["srcs"],
  data: () => ({
    index: 0,
  }),

  created() {
    this.index = Math.floor(Math.random() * this.srcs.length);
  },

  methods: {
    next() {
      if (this.index >= this.srcs.length - 1) this.index == 0;
      else ++this.index;
    },
  },
};
</script>

<style lang="postcss">
svg {
  @apply h-8 w-8;
}
</style>