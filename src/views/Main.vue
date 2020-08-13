<template>
  <div id="Main">
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
      page_len:2
    }
  },
  mounted(){
    window.addEventListener('wheel',(e)=>{
      console.log(e.wheelDelta);
      if(e.wheelDelta > 0){
        console.log('위로')
        if (this.cur_page > 0){
          this.cur_page -= 1
        }
      } else {
        console.log('아래로')
        if (this.cur_page < this.page_len-1){
          this.cur_page += 1
        }
      }
    })
  }
}
</script>

<style lang="scss">
#Main{
  width: 100%;
  height: 100%;
}
</style>
