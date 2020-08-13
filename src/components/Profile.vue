<template>
  <div id="profile">
      <div class="title">학력사항</div>
      <DL class="line" :data="school"/>
      <div class="title">교육과정</div>
      <DL class="line" :data="edu"></DL>
      <div class="title">수상경력</div>
      <DL class="line" :data="award"></DL>
      <div class="title">자격사항</div>
      <DL class="line" :data="license"></DL>

  </div>
</template>

<script>
import DL from './DateLine.vue'
export default {
    components:{
        DL
    },
    data(){
        return{
            school:[
            {'date':'2008.03 ~ 2011.02', 'content':'광신고등학교'},
            {'date':'2012.03 ~ 2020.08', 'content':'인하대학교 산업공학 전공'},
            ],
            edu:[{'date':'2016.12 ~ 2017.02', 'content':'SW융합 서비스 기획과 시큐어 코딩 융합 전문가 양성과정 6'},
            {'date':'2019.07 ~ 2020.06', 'content':'삼성 청년 SW 아카데미'},
            ],
            award:[
                {'date':'2019.12.02','content':'제 2회 빅스비 캡슐 챌린지 입선'},
                {'date':'2020.06.15','content':'SSAFY 심화 프로젝트 서울 2등'},
            ],
            license:[
                {'date':'2018.08.17','content':'정보처리기사'},
                {'date':'2019.11.16','content':'삼성전자 상시 소프트웨어 역량 테스트 A등급'},
            ]
        }
    }
}
</script>

<style lang='scss'>
#profile{
    position: absolute;
    width: 80%;
    height: 80%;
    left: 10%;
    top: 10%;
    .title{
        font-size: 25px;
        font-weight: bold;
        margin-left: 20px;
    }
    .line{
        margin-top: 15px;
        margin-bottom: 30px;
        margin-left: 35px;
    }
}

</style>