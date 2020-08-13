<template>
  <div id="starRating">
      <img class="star" src="../assets/img/star.png" alt="" v-for="i in score" :key="i">
  </div>
</template>

<script>
export default {
    props:{
        score:Number
    }
}
</script>

<style lang="scss">
#starRating{
    display: flex;
    justify-content: flex-start;
    margin-left: 15px;
    .star{
        width: 40px;
        height: 40px;
    }
}
</style>
