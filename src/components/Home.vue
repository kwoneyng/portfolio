<template>
  <div id="home">
    <div id="portfolioText">Portfolio</div>
    <IS/>
  </div>
</template>

<script>
// @ is an alias to /src
import IS from './InfoSet'
export default {
  name: 'Home',
  components: {
      IS,
  },
}
</script>

<style lang="scss">
#home{
  position: absolute;
  width: 1300px;
  height: 750px;
  left: 10%;
  top: 10%;
  border-radius: 30px;
  background-color: white;

  #portfolioText{
    position :absolute;
    font-size: 100px;
    top: 5%;
    left: 5%;
  }
}
</style>
