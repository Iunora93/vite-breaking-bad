<script>
import { store } from "../store.js";
import AppCard from './AppCard.vue';

export default {
  name: "AppSection",
  components:{
    AppCard,
  },
  data() {
    return {
      store,
    };
  },
  computed: {
    totalCharaters() {
      return this.store.characters.length;
    },
  },
};
</script>

<template>
    <main>
     <div class="container-lg py-4 px-5">
        <div class="container-sm">
            <h6 class="py-3 px-3">Found {{totalCharaters}} characters</h6>           
        </div>
        <div class="container-sm d-flex justify-content-center">
            
                <AppCard 
                v-for="character in store.characters"
                class=" m-2 my-col"           
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
        .my-col{
          width: calc(100% - 32px);
          @include media-breakpoint-up(sm) {
            width: calc(50% - 32px);
          }
          @include media-breakpoint-up(md) {
            width: calc((100% / 3) - 32px);
          }
          @include media-breakpoint-up(lg) {
            width: calc(20% - 32px);
          }
              }
        }
}
</style>