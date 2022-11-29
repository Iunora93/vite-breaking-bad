<script>
import axios from "axios";
import { store } from "../store.js";
import AppSearch from './AppSearch.vue';
import AppSection from './AppSection.vue';

export default {
  name: "AppMain",
  components: {
    AppSearch,
    AppSection,
  },
  data(){
    return{
      store,
    };
  },
  methods: {
    getCharacters(){
      axios
        .get("https://www.breakingbadapi.com/api/characters", {
          params: {
            category: this.store.statusCategory,
          },
        })
        .then((resp) => {
          this.store.characters = resp.data;
        })
        .catch((err) => {
          this.store.characters = [];
        });
    }
  },
  created() {
    this.getCharacters();
  },
};
</script>

<template>
    <main>
      <AppSearch @search="getCharacters"/>
      <AppSection />
    </main>
</template>

<style  lang="scss" scoped>
@import './src/style/variables.scss';
</style>