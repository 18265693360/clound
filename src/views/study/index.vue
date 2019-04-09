<!--<template>-->
<!--<template>-->
<!--<div class="read-item">-->
<!--<div class="read-left" v-for="(it, index) in options.book" :key="index">-->
<!--&lt;!&ndash;记得绑定 v-bind 绑定两个src alt 这样it 才不会undefined&ndash;&gt;-->
<!--<img src="#" alt="">-->
<!--</div>-->
<!--<div class="read-right">-->
<!--<div class="title">-->

<!--</div>-->
<!--<div class="where">-->
<!---->
<!--</div>-->
<!--<div class="last-msg"></div>-->
<!--<div class="btns">-->
<!--<Button type="default" size="small">继续阅读</Button>-->
<!--<Button type="default" size="small">查看文档</Button>-->
<!--</div>-->
<!--</div>-->
<!--</div>-->
<!--</template>-->

<!--<script>-->
<!--export default {-->
<!--name: "readListData",-->
<!--props:{-->
<!--options:Object-->
<!--},-->
<!--created() {-->
<!--console.log(this.options);-->
<!--},-->
<!--}-->
<!--</script>-->
<!--<style scoped lang="scss" src="./index.scss"></style>-->
  <!--<div class="container study">-->
    <!--<div class="text">我的学习</div>-->
    <!--<div class="read">-->
      <!--<ReadListData v-for="(item,index) in readListData"-->
                        <!--:options="item"-->
                        <!--:key="index"/>-->
    <!--</div>-->
    <!--&lt;!&ndash;这是引入的底部tap-bar&ndash;&gt;-->
    <!--<DyTabbar page="study"></DyTabbar>-->
  <!--</div>-->
<!--</template>-->
<!--<script>-->
  <!--import ReadListData from './components/readListData'-->
  <!--import { Button } from 'mint-ui';-->
  <!--import DyTabbar from '@/components/tab-bar'-->
  <!--import moment from 'moment'-->
  <!--// 这是引入的tab-bar-->
  <!--export default {-->
    <!--name: "study",-->
    <!--// 定义父子传值-->
    <!--props:{-->
      <!--options:Object-->
    <!--},-->
    <!--components:{-->
      <!--// 声明的tab-bar-->
      <!--ReadListData,-->
      <!--DyTabbar,-->
      <!--Button-->
    <!--},-->
    <!--data(){-->
      <!--return{-->
        <!--readListData:[]-->
      <!--}-->
    <!--},-->
    <!--methods:{-->
      <!--getReadList(){-->
        <!--this.$axios.get(this.$api.getReadList).then(res=>{-->
          <!--this.readListData = res.data-->
          <!--// 打印数据-->
          <!--console.log(res);-->
        <!--})-->
      <!--}-->
    <!--},-->
    <!--created() {-->
      <!--this.getReadList()-->
    <!--}-->
  <!--}-->
<!--</script>-->
<!--<style scoped lang="scss">-->
<!--</style>-->
<template>
  <!--注意这里的 my-learn在引号中间-->
  <div class="container my-learn">
    <div class="my-learn-item">
      <div class="img-wrap">
        <img src="../../assets/p1.jpg" alt="">
      </div>

      <div class="book-msg">
        <h2 class="title">
          SASS中文教程
        </h2>
        <div class="read-msg">
          书籍3/5章节
        </div>
        <div class="progress-wrap">
          <progress  :value="20" :bar-height="5" style="background: lawngreen;"></progress>
          <div class="progress-item">
            已看60%
          </div>
        </div>
        <div class="recent-read-item">
          <div class="recent-read">
            上次查看:安装SASS
          </div>
          <div class="recent-read-day">
            13天前
          </div>
        </div>
        <div class="btns-wrap">
          <Button type="default" size="small">继续阅读</Button>
          <Button type="default" size="small">查看文档</Button>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
  import {Button, Progress} from 'mint-ui';

  export default {
    name: "index",
    components:{
      Button,
      Progress,
    }
  }
</script>

<style scoped lang="scss" src="./index.scss"></style>


