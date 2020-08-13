<template>
  <div id="app" :style="{width:width+'px', height:height+'px'}" >
    <div id="nav"></div>
    <router-view/>
  </div>
</template>

<script>
export default {
  data(){
    return{
      width:window.innerWidth,
      height:window.innerHeight,
    }
  },
  mounted(){
  }
}
</script>

<style lang="scss">
#app{
  margin: 0;
}
</style>
