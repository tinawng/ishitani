<template>
  <div class="nav-container">
    <h2>ishitani furniture</h2>
    <div class="nav-menu">
      <h3>design</h3>
      <h3>shop</h3>
      <h3>diary</h3>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style lang="postcss" scoped>
.nav-container {
  @apply m-8;
  @apply flex justify-between items-center;
}

.nav-menu {
    @apply flex items-center
}
.nav-menu h3 {
    @apply mx-8;
}
</style>