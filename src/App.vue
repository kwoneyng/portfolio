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
      width:document.body.clientWidth,
      height:document.body.clientHeight
    }
  },
  mounted(){
    console.log(this.width, this.height)
  }
}
</script>

<style lang="scss">
#app{
  margin: 0;
}
</style>
