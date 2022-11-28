<script>
export default {
  name: "AppCard",
  
  props: {
    info: Object,
  }, 
  data() {
    return {
      characters: [],
    };
  },
  created() {
    axios.get("https://www.breakingbadapi.com/api/characters").then((resp) => {
      this.characters = resp.data.results;
    });
  }, 
};
</script>

<template> 
<main class="d-flex">
    <div class="text-center px-2 py-2 mx-3"  v-for="character in characters">
        <img class="img-fluid" src="" alt="" />
        <h5 class="mb-3">{{character.name}}</h5>
        <div class="status"></div>
        <div class="race"></div>
    </div>
</main>
</template>

<style lang="scss" scoped>
    .text-center{
        background-color: var(--primary-color);
        h5{
            color: white;
        }
        .status, .race{
            color: gray;
            font-size: 13px;
        }
    }
</style>