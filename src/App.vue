<template>
  <div id="app">

     <div class = "upper">
         <div class = "headline"> Hi, 和我一起开始你的专注之旅</div>
        <img id = "cat" src= "@/assets/Whitecat.png" >
    </div>

    <div class="loginUI">
       <login></login>
       
    </div>

  </div>
 
</template>

<script>
import login from '@/views/login.vue';
//registration
export default{
  name:'app',
  components:{
    login
  }
}
</script>

<style>
*{
  margin:0;
}
.loginUI{
    background-color:#F98C93;
    border-radius: 27px;
    position: absolute; bottom:0;
    left:0;
    width:100%;
}

.headline{
  padding: 20px;
}
html{
  height:100%;
}
.upper{
  background: #56D4C0;
  color: white;
  font-size:20px;
  font-family: PingFangSC-Regular, sans-serif;
  width: 100%;
  height:350px;

  /* 垂直居中 */
  display: flex;
  flex-direction: column;
  align-items: center; 
  justify-content: center; 
  
}
#cat{
  width: 119px;
  height: 103px;
  background-color: #56D4C0;
  
}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center; 
  color:white;
  
}


</style>
