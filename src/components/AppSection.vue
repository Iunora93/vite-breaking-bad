<script>
import axios from "axios";
import AppCard from './AppCard.vue';

export default {
  name: "AppSection",
  components:{
    AppCard,
  },
  data() {
    return {
      characters: [],
    };
  },
  created() {
    axios.get("https://www.breakingbadapi.com/api/characters").then((resp) => {
      this.characters = resp.data;
    });
  },
};
</script>

<template>
    <main>
     <div class="container-lg py-4 px-5">
        <div class="container-sm">
            <h6 class="py-3 px-3">Found 62 characters</h6>           
        </div>
        <div class="container-sm d-flex">
            
                <AppCard 
                v-for="character in characters"
                class="col-lg-2"           
                :info="character"
                />
            
        </div>
     </div> 
      
    </main>
</template>

<style  lang="scss" scoped>

.container-lg{
    background-color: var(--secondary-color);
    .container-sm{
        flex-wrap: wrap;
        h6{
            color: white;
            background-color: #212529;
        }
    }
}
</style>