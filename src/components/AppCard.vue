<script>
export default {
  name: "AppCard", 
  props: {
    info: Object,
  }, 
};
</script>

<template> 

    <div class="text-center px-3 py-3 mx-3 mb-2">
        <img class="img-fluid mb-2" :src="info.img" alt="" />
        <h5 class="mb-2">{{info.name}}</h5>
        <h6 class="category">{{info.category}}</h6>
        <div class="status">{{info.status}}</div>
    </div>

</template>

<style lang="scss" scoped>
    .text-center{
        background-color: var(--primary-color);
        
        h5{
            color: white;
        }
        .status, .category{
            color: gray;
            font-size: 13px;
        }
    }
</style>