<template>
  <div id="profile">
      <div class="info">
          <img class="pic" src="../assets/img/profile.jpg" alt="">
          <IS/>
          <p class="skillTitle">기술 스택</p>
          <div class="skill1">
            <div class="label">python</div>
            <div class="skillSet">
                <img class="skillIcon" src="../assets/img/python.png" alt="">
                <SR :score="skillScore[0]"/>
            </div>
            <div class="label">vue</div>
            <div class="skillSet">
                <img class="skillIcon" src="../assets/img/vue.png" alt="">
                <SR :score="skillScore[1]"/>
            </div>
            <div class="label">nodejs</div>
            <div class="skillSet">
                <img class="skillIcon" src="../assets/img/nodejs.png" alt="">
                <SR :score="skillScore[2]"/>
            </div>
          </div>
          <div class="skill2">
            <div class="label">android studio</div>
            <div class="skillSet">
                <img class="skillIcon" src="../assets/img/android.png" alt="">
                <SR :score="skillScore[3]"/>
            </div>
            <div class="label">kotlin</div>
            <div class="skillSet">
                <img class="skillIcon" src="../assets/img/kotlin.png" alt="">
                <SR :score="skillScore[4]"/>
            </div>
          </div>
      </div>
      <div class="content">
        <div class="title">학력사항</div>
        <DL class="line" :data="school"/>
        <div class="title">교육과정</div>
        <DL class="line" :data="edu"></DL>
        <div class="title">수상경력</div>
        <DL class="line" :data="award"></DL>
        <div class="title">자격사항</div>
        <DL class="line" :data="license"></DL>
      </div>

  </div>
</template>

<script>
import DL from './DateLine.vue'
import SR from './StarRating'
import IS from './ProfileInfoSet'
export default {
    components:{
        DL,SR,IS
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
            ],
            skillScore:[4,4,3,3,3]
        }
    }
}
</script>

<style lang='scss'>
#profile{
    position: absolute;
    width: 1300px;
    min-width: 1200px;
    min-height: 650px;
    height: 750px;
    top:10%;
    left:10%;
    background-color: white;
    border-radius: 30px;
    .info{
        position: absolute;
        width: 40%;
        left: 60%;
        top: 5%;
        height: 90%;
        .skillTitle{
            position: absolute;
            top:33%;
            width: 200px;
            font-size: 25px;
            font-weight: bold;
            margin-bottom: 20px;
        }
        .skill{
            &1{
                position: absolute;
                top:45%;
                left: 30px;
                .label{
                    font-size: 12px;
                    font-weight: bold;
                    margin-bottom: 3px;
                }
                .skillSet{
                    display: flex;
                    justify-content: flex-start;
                    margin-bottom: 20px;
                    .skillIcon{
                        width: 40px;
                        height: 40px;
                        object-fit: cover;
                    }
                }
            }
            &2{
                position: absolute;
                top:45%;
                left: 280px;
                .label{
                    font-size: 12px;
                    font-weight: bold;
                    margin-bottom: 3px;
                }
                .skillSet{
                    display: flex;
                    justify-content: flex-start;
                    margin-bottom: 20px;
                    .skillIcon{
                        width: 40px;
                        height: 40px;
                        object-fit: cover;
                    }
                }

            }
        }
        .pic{
            position: absolute;
            width: 200px;
            left: 250px;
            border-radius: 50%;
        }
    }
    .content{
        position: absolute;
        width: 50%;
        height: 80%;
        top: 10%;
        left: 5%;
        .title{
            font-size: 25px;
            font-weight: bold;
        }
        .line{
            margin-top: 15px;
            margin-bottom: 50px;
            margin-left: 15px;
        }
    }
}

</style>