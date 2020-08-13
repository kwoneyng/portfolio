<template>
  <div id="main">
    <Home v-if="cur_page == 0"/>
    <Profile v-if="cur_page == 1"/>
  </div>
</template>

<script>
// @ is an alias to /src
import Home from '../components/Home'
import Profile from '../components/Profile'

export default {
  components: {
    Home,Profile
  },
  data(){
    return{
      cur_page:1,
      page_len:2,
      pages:['home','profile'],
      delay:0
    }
  },
  methods:{
    resize(){
      var back = document.getElementById('main')
      back.style.width = window.innerWidth + 'px'
      back.style.height = window.innerHeight + 'px'
      var card = document.getElementById(this.pages[this.cur_page])
      card.style.left = (window.innerWidth - 1300)/2 +'px'
      card.style.top = (window.innerHeight - 750)/2 +'px'
    }
  },
  mounted(){
    this.resize()
    window.addEventListener('resize',(e)=>{
      this.width = e.target.innerWidth
      this.height = e.target.innerHeight
      this.resize()
    })

    window.addEventListener('wheel',(e)=>{
      var time = new Date().getTime()
      if (time - this.delay > 500){
        this.delay = time
        if(e.wheelDelta > 0){
          if (this.cur_page > 0){
            this.cur_page -= 1
          }
        } else {
          if (this.cur_page < this.page_len-1){
            this.cur_page += 1
          }
        }
      }
    })
  },
  watch:{
    cur_page:function(){
      this.resize()
    }

  }
}
</script>

<style lang="scss">
#main{
  width: 100%;
  height: 100%;
  background-color: #dddddd;
}
</style>