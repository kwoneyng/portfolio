<template>
  <div id="infoSet">
      <div class="vline"></div>
      <div class="nameKR">박권응</div>
      <div class="nameEN">PARK KWONEYNG</div>
      <div class="email">nan308@kakao.com</div>
      <div class="phone">010-7760-6820</div>
    </div>
</template>

<script>
export default {

}
</script>

<style lang='scss'>
#infoSet{
    position: absolute;
    right: 5%;
    bottom: 5%;
    width: 300px;
    height: 160px;
    .vline{
      position: absolute;
      width: 2px;
      height: 90%;
      top: 5%;
      background-color: #888888;
    }
    .nameKR{
      position: absolute;
      left: 10px;
      font-size: 40px;
      font-weight: bold;
    }
    .nameEN{
      position: absolute;
      left: 10px;
      top:50px;
      font-size: 30px;
      font-weight: bold;
    }
    .email{
      position: absolute;
      left: 10px;
      top: 95px;
      font-size: 25px;
    }
    .phone{
      position: absolute;
      left: 10px;
      top: 125px;
      font-size: 25px;
    }
}
</style>