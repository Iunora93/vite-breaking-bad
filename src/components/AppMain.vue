<script>
import AppSearch from './AppSearch.vue';
import AppSection from './AppSection.vue';

export default {
  name: "AppMain",
  components: {
    AppSearch,
    AppSection,
  },
};
</script>

<template>
    <main>
      <AppSearch />
      <AppSection />
    </main>
</template>

<style  lang="scss" scoped>
@import './src/style/variables.scss';
</style>