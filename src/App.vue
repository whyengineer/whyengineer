<template>
  <div class="bg">
    <bg :win-height="winHeight" :win-width="winWidth"></bg>
    <img src="https://img.whyengineer.com/logo.png?imageView2/1/w/300/h/300/q/100|imageslim" class="logo" :style="ls">
    <div class="name" :style="names">WhyEngineer</div>
    <div class="nav" :style="ns">
      <el-row>
        <el-button  round class="index" @click="forumHandle"><i class="fab fa-blogger" ></i> 论坛</el-button>
        <el-button  round class="index"  @click="githubHandle"><i class="fab fa-github"></i> Github</el-button>
        <el-button  round class="index" @click="taobaoHandle"><i class="fas fa-shopping-cart" ></i> 淘宝</el-button>
      </el-row>
    </div>
  </div>
</template>

<script>
import bg from "./background.vue"


export default {
  components:{
    bg,
  },
  name: 'app',
  data () {
    return{
      winWidth: document.documentElement.clientWidth,
      winHeight:document.documentElement.clientHeight,
      ls:{},
      ns:{},
      names:{}
    }
  },
   methods: {
        handleWindowResize(event) { 
            this.winWidth = event.currentTarget.innerWidth; 
            this.winHeight=event.currentTarget.innerHeight;
        },
        githubHandle(){
          window.open("https://github.com/whyengineer")
        },
        taobaoHandle(){
          window.open("https://shop589999598.taobao.com/index.htm?spm=2013.1.w5002-16739521491.2.43275cf8ZsMdzw")
        },
        forumHandle(){
          window.open("https://forum.whyengineer.com")
        }
    },
    beforeDestroy: function () {
        window.removeEventListener('resize', this. handleWindowResize)
    },
    mounted() {
        window.addEventListener('resize', this.handleWindowResize);
        this.ls={
          top:this.winHeight/2-300+'px',
          left:this.winWidth/2-170+'px'
        }
        this.ns={
          top:this.winHeight/2+250+'px',
          left:this.winWidth/2-300+'px'
        }
        this.names={
          top:this.winHeight/2+25+'px',
          left:this.winWidth/2-280+'px'
        }
    },
}
</script>
<style>
 body{
   padding: 0px;
   margin: 0px;
 }
 .name{
   position: absolute;
   top:0px;
   left: 0px;
   font-size: 100px;
   font-family: Impact, Charcoal, sans-serif;
 }
 .index{
   margin-left: 30px;
   margin-right: 30px;
   width: 150px;
   font-size: 20px;
   text-align: center;
 }
 .logo{
   position: absolute;
   top: 0px;
   left: 0px;
 }
 .nav{
   position: absolute;
   top: 0px;
   left: 0px;
 }
 .bg{
   background-color:rgb(245, 240, 240);
 }
</style>



