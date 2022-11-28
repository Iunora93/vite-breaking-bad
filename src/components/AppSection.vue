<script>
import AppCard from './AppCard.vue';
import axios from "axios";

export default {
  name: "AppSection",
  components:{
    AppCard,
  },
  
};
</script>

<template>
    <main>
     <div class="container-lg py-4 px-5">
        <div class="container-sm">
            <h6 class="py-3 px-3">Found 62 characters</h6>           
        </div>
        <div class="container-sm">
            <AppCard 
            />
        </div>
     </div> 
      
    </main>
</template>

<style  lang="scss" scoped>

.container-lg{
    background-color: var(--secondary-color);
    .container-sm{
        
        h6{
            color: white;
            background-color: #212529;
        }
    }
}
</style>