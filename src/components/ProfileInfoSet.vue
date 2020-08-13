<template>
  <div id="profileInfoSet">
      <div class="vline"></div>
      <div class="detail">
        <div class="nameKR">박권응</div>
        <div class="nameEN">PARK KWONEYNG</div>
        <div class="birth">1992.11.26</div>
        <div class="email">nan308@kakao.com</div>
        <div class="phone">010-7760-6820</div>
      </div>
    </div>
</template>

<script>
export default {

}
</script>

<style lang='scss'>
#profileInfoSet{
    position: absolute;
    left: 0;
    top:5%;
    width: 300px;
    height: 160px;
    .vline{
        position: absolute;
        width: 2px; 
        height: 125px;
        top: 5px;
        background-color: #888888;
    }
    .detail{
        margin-left: 10px;
        font-size: 16px;
    }
    .nameKR{
      font-size: 26px;
      font-weight: bold;
    }
    .nameEN{
      font-size: 20px;
      font-weight: bold;
      margin-bottom: 8px;
    }
}
</style>