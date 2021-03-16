<template>
  <div class="wrapper" ref="aaaa">

    <ul class="content">
      <li>分类列表1</li>
      <li>分类列表2</li>
      <li>分类列表3</li>
      <li>分类列表4</li>
      <li>分类列表5</li>
      <li>分类列表6</li>
      <li>分类列表7</li>
      <li>分类列表8</li>
      <li>分类列表9</li>
      <li>分类列表0</li>
      <li>分类列表</li>
      <li>分类列表</li>
      <li>分类列表</li>
      <li>分类列表</li>
      <li>分类列表</li>
      <li>分类列表</li>
      <li>分类列表</li>
      <li>分类列表</li>
      <li>分类列表</li>
      <li>分类列表</li>
      <li>分类列表</li>
      <li>分类列表</li>
      <li>分类列表</li>
      <li>分类列表</li>
      <li>分类列表</li>
      <li>分类列表</li>
      <li>分类列表</li>
      <li>分类列表</li>
      <li>分类列表</li>
      <li>分类列表</li>
      <li>分类列表</li>
      <li>分类列表</li>
      <li>分类列表</li>
      <li>分类列表</li>
      <li>分类列表</li>
      <li>分类列表</li>
      <li>分类列表</li>
      <li>分类列表</li>
      <li>分类列表</li>
      <li>分类列表</li>
      <li>分类列表</li>
      <li>分类列表</li>
      <li>分类列表</li>
      <li>分类列表</li>
      <li>分类列表</li>
      <li>分类列表</li>
      <li>分类列表</li>
      <li>分类列表</li>
      <li>分类列表</li>
      <li>分类列表</li>
      <li>分类列表</li>
      <li>分类列表</li>
      <li>分类列表</li>
      <li>分类列表</li>
      <li>分类列表</li>
      <li>分类列表</li>
      <li>分类列表</li>
      <li>分类列表</li>
      <li>分类列表</li>
      <li>分类列表</li>
      <li>分类列表</li>
      <li>分类列表</li>
      <li>分类列表</li>
      <li>分类列表</li>
      <li>分类列表</li>
      <li>分类列表</li>
      <li>分类列表</li>
      <li>分类列表</li>
      <li>分类列表</li>
      <li>分类列表</li>
      <li>分类列表</li>
      <li>分类列表</li>
      <li>分类列表</li>
      <li>分类列表</li>
      <li>分类列表</li>
      <li>分类列表</li>
      <li>分类列表</li>
      <li>分类列表</li>
      <li>分类列表</li>
      <li>分类列表</li>
      <li>分类列表</li>
      <li>分类列表</li>
      <li>分类列表</li>
      <li>分类列表</li>
      <li>分类列表</li>
      <li>分类列表</li>
      <li>分类列表</li>
      <li>分类列表</li>
      <li>分类列表</li>
      <li>分类列表</li>
      <li>分类列表</li>
      <li>分类列表</li>
      <li>分类列表</li>
      <li>分类列表</li>
      <li>分类列表</li>
      <li>分类列表</li>
      <li>分类列表</li>
      <li>分类列表</li>
      <li>分类列表</li>
      <li>分类列表</li>
      <li>分类列表</li>
      <li>分类列表</li>
      <li>分类列表</li>
      <li>分类列表</li>
      <li>分类列表</li>
      <li>分类列表</li>
      <li>分类列表</li>
      <li>分类列表</li>
      <li>分类列表</li>
      <li>分类列表</li>

    </ul>

  </div>
</template>

<script>
  import BScroll from 'better-scroll'
  export default {
    name: "Category",
    data(){
      return{
        scroll:null
      }
    },

    mounted(){
      this.scroll = new BScroll(document.querySelector('.wrapper'),{
        probeType:3,
        pullUpload:true,
        click:true
      })

      this.scroll.on('scroll',(position) =>{
        console.log(position)
      })

      this.scroll.on("pullingUp", ()=>{
        console.log('上拉加载更多');
      })
    }
  }
</script>

<style scoped>
  .wrapper {
    height:150px;
    background-color: red;

    overflow:hidden;
    /*overflow-y:scroll;*/
  }
</style>
