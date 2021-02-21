<template>
  <div class="nav-container">
    <h2>ishitani furniture</h2>
    <div class="nav-menu">
      <h3>design</h3>
      <h3 class="muted">shop</h3>
      <h3 class="muted">diary</h3>
    </div>
    <div class="nav-lang">
      <h3>en</h3>
      <h3 class="muted">日本語</h3>
    </div>
  </div>
</template>


<script>
export default {
  data: () => ({
    show_nav: false,
  }),
  methods: {
    scrollTo(section_name) {
      var el = this.$parent.$parent.$el.getElementsByClassName(section_name)[0];
      el.scrollIntoView({behavior: "smooth"});
    }
  }
};
</script>

<style lang="postcss" scoped>
.nav-container {
  @apply m-8;
  @apply flex items-center;
}
.nav-container > :first-child {
  @apply w-1/2;
}
.nav-container > * {
  @apply w-1/4;
}

.nav-menu,
.nav-lang {
  @apply flex;
}
.nav-menu {
  @apply justify-around;
}
.nav-lang {
  @apply justify-end;
}
.nav-lang h3:not(:last-child) {
  @apply mr-6;
}

h3 {
  @apply cursor-pointer;

  transition: all 0.3s;
  transition-property: color, opacity;
}
h3:hover {
  @apply text-black opacity-100;
}

.muted {
  @apply text-coal-700 opacity-40;
}
</style>