<script>
export default {
  name: "AppHeader",
};
</script>

<template>
  <header>
    <h1>header</h1>
  </header>
</template>

<style lang="scss" scoped>
h1 {
  @include media-breakpoint-up(md) {
    color: green;
  }
}
</style>
