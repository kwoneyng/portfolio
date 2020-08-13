<template>
  <div id="home">
    <div id="portfolioText">Portfolio</div>
    <div id="infoSet">
      <div class="vline"></div>
      <div class="nameKR">박권응</div>
      <div class="nameEN">PARK KWONEYNG</div>
      <div class="email">nan308@kakao.com</div>
      <div class="phone">010-7760-6820</div>
    </div>
  </div>
</template>

<script>
// @ is an alias to /src

export default {
  name: 'Home',
  components: {
  },
}
</script>

<style lang="scss">
#home{
  position: absolute;
  width: 80%;
  height: 100%;
  left: 10%;

  #portfolioText{
    position :absolute;
    font-size: 100px;
    top: 5%;
    left: 5%;
  }
  #infoSet{
    position: absolute;
    right: 5%;
    bottom: 5%;
    width: 300px;
    height: 160px;
    .vline{
      position: absolute;
      width: 4px;
      height: 100%;
      background-color: #cccccc;
    }
    .nameKR{
      position: absolute;
      left: 20px;
      font-size: 40px;
      font-weight: bold;
    }
    .nameEN{
      position: absolute;
      left: 20px;
      top:50px;
      font-size: 30px;
      font-weight: bold;
    }
    .email{
      position: absolute;
      left: 20px;
      top: 95px;
      font-size: 25px;
    }
    .phone{
      position: absolute;
      left: 20px;
      top: 125px;
      font-size: 25px;
    }
  }

}
</style>
