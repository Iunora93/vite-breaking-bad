<script>
export default {
  name: "AppCard", 
  props: {
    info: Object,
  }, 
};
</script>

<template> 
<main class="d-flex">
    <div class="text-center px-2 py-2 mx-3 mb-2">
        <img class="img-fluid" :src="info.img" alt="" />
        <h5 class="mb-3">{{info.name}}</h5>
        <div class="status">{{info.status}}</div>
    </div>
</main>
</template>

<style lang="scss" scoped>
    .text-center{
        background-color: var(--primary-color);
        width: 200px;

        img{
            width: 100px;
        }
        h5{
            color: white;
        }
        .status, .race{
            color: gray;
            font-size: 13px;
        }
    }
</style>