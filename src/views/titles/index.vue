<template>
    <div class="container">
      <ul class="titles">
        <li class="title-item" v-for = "(item,index) in titles" :key="index">
          <router-link :to="{name:'article', params:{id: item._id}}">
            <!--{{item.titles}}多了一个's'-->
            {{item.title}}
          </router-link>
        </li>
      </ul>
    </div>
</template>

<script>
  export default {
    name: "titles",
    data(){
      return{
        titles:[],
        bookData:{}
      }
    },
    methods:{
      //gitTitles需要api 去接口那里调取 去api中设置
      getTitles () {
        const id = this.$route.params.id
        this.$axios.get(this.$api.getTitles + id).then(res =>{
          // 设置跳转到相应页面 地址栏有相对的名字
          console.log(res);
          this.titles = res.data
        })
      },
      getBookData (){
        const id = this.$route.params.id
        this.$axios.get(this.$api.getBook + id).then(res => {
          // 设置跳转到相应页面 地址栏有相对的名字
          let resData = res.data;
          this.bookData = resData;
          document.title = resData.title + '__' + '目录'
        })
      }
    },
    created() {
      this.getTitles()
      this.getBookData()
    }
  }
</script>

<style scoped lang="scss">
  .title-item{
    line-height: 40px;
    height: 40px;
    padding-left: 10px;
    border-bottom:1px solid #e0e0e0;

    a{
      color: #333333;
    }
  }
  //a标签就是 router-link

</style>



