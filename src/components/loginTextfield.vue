
<template>
<div class="loginTextfield">
    
      <h1>Welcome</h1>
      <input id="phoneNum" type="text" placeholder="请输入手机号码"/>
        <div class="verification">

        <input id="verification" type="text" placeholder="请输入验证码"/>
            <div id="sendCode">
                <input v-if= "isSend" v-on:click="sendCode()" id="code" type="button" value="发送"/>
                <span v-else> {{countdown}}</span>
            </div>
        </div>

      <input id="submit" type="button" value="登陆/注册"/>
    
</div>
</template>
   


<script>



export default{
    name:'loginTextfield',
    data(){
        return{
            isSend: true,
            countdown:60,
        }
    },
    methods: {
        sendCode: function(){
           this.isSend =  false
           let timer = setInterval(() => {
               this.countdown -- ;
               if(this.countdown <= 0 ){
                   this.isSend = true
                   clearInterval(timer)
                   this.countdown =  60
               }
           }, 1000)
        }
    }
    
}
</script>


<style scoped>
span{
    width: 61px;
    height: 70px;
    margin: 13px;
    background-color: #56D4C0;
    border: 2px solid white;
    border-radius: 15px;
    display:inline-block;
    line-height:70px;
    

}
.verification{
    background-color:#F98C93;
    display:flex;
    flex-direction: row;
   
}
#verification{
    width: 182px;
    
}
#code{
    width:61px;
    padding:0;
    background-color:#56D4C0 ;
}
#submit{
    background-color:#56D4C0 ;
    font-size:20px;
}
.loginTextfield{

    display: flex;
    flex-direction: column;
    align-items: center; 
    justify-content: center; 
    margin:40px;
    background-color:#F98C93;
    border-radius: 27px;
    transition:all .6s ease;
}
h1,label{
    background-color: #F98C93;

}
h1{
    margin-top:10px;
    margin-bottom:20px;
}
input{
   background-color:#F98C93;
   color:white;

   border-radius: 15px;
   padding: 20px;
   margin: 13px;
 
   border-color:white;


   border-style:solid;
   width: 270px;
   height: 70px;

   box-sizing: border-box;}

input::-webkit-input-placeholder{
    color: rgb(255,255,255,60)
}
input::-moz-placeholder{   /* Mozilla Firefox 19+ */
    color:rgb(255,255,255,60)
}
input:-moz-placeholder{    /* Mozilla Firefox 4 to 18 */
    color:rgb(255,255,255,60)
}
input:-ms-input-placeholder{  /* Internet Explorer 10-11 */ 
    color:rgb(255,255,255,60)
}
</style>
