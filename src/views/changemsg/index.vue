<!--这个路由也是和其他views文件平级 不和person一个级别-->
<template>
    <div class="container changemsg">

     <div class="nav">
       <div class="nav-item">
           <!--<i class="iconfont icon-fanhui1"></i>-->
           <!--<div class="desc">返回</div>-->
         <Button class="back" icon="back" @click="hundleJumpP">返回</Button>
       </div>
       <div class="nav-item change">修改个人信息</div>
     </div>


      <div class="msg">
        <div class="msg-item">
          <div class="detail head">头像</div>
          <div class="item">
            <img src="../../assets/fortruth.jpg" alt="">
            <i class="iconfont icon-fanhui icon1"></i>
          </div>
        </div>

        <div class="liner"></div>

        <div class="msg-item">
          <div class="detail nickname">昵称</div>
          <div class="item">
            <p>1243324</p>
            <i class="iconfont icon-fanhui"></i>
          </div>
        </div>

        <div class="liner"></div>

        <div class="msg-item">
          <div class="detail sign">个性签名</div>
          <div class="item">
            <p>未填写任何内容</p>
            <i class="iconfont icon-fanhui"></i>
          </div>
        </div>

        <div class="liner"></div>

        <div class="msg-item">
          <div class="detail pass">修改密码</div>
          <div class="item">
            <i class="iconfont icon-fanhui"></i>
          </div>
        </div>

      </div>
    </div>
</template>

<script>
  import { Button } from 'mint-ui';

    export default {
        name: "changemsg",
      components:{
          Button
      },
      methods:{
        hundleJumpP(){
          this.$router.push({
            name:'personal'
          })
        }
      }
    }
</script>

<!--老生常言 加 ./-->
<style scoped lang="scss" src="./index.scss"></style>
