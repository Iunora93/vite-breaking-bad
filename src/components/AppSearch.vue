<script>
import { store } from "../store.js";
export default {
  name: "AppSearch",
  data(){
    return{
    store,
    };
  },
};
</script>

<template>
    <main>
     <div class="container">
        <div class="col-auto mt-3 mb-3">
            <select class="form-select w-auto" v-model="store.statusCategory" @change="$emit('search')">           
                <option selected value="">Select category</option>
                <option value="Breaking Bad">Breaking Bad</option>
                <option value="Better Call Saul">Better Call Saul</option>
                <option value="Breaking Bad, Better Call Saul">Breaking Bad & Better Call Saul</option>
            </select>
        </div>
     </div> 
      
    </main>
</template>

<style  lang="scss" scoped>
</style>