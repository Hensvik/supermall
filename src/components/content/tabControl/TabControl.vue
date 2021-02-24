<template>
  <div class="tab-control">
      <div v-for="(item,index) in titles" class="tab-control-item" :key="item" :class="{active:index === currentIndex}">
      <span>{{item}}</span>
    </div>
    <div><span></span></div>
    <div><span></span></div>
  </div>
</template>

<script>
  export default {
    name: "tabControl",
    props:{
      titles:{
        type:Array,
        default(){
          return []
        }
      }
    },

  }
</script>

<style scoped>
  .tab-control{
    display:flex;
    text-align:center;
    font-size:15px;
    height:40px;
    line-height:40px;
  }

  .tab-control-item{
    flex:1;
  }

  .tab-control-item span{
    padding:5px;
  }

  .active{
    color:var(--color-high-text);
  }

  .active span{
    border-bottom: 3px solid var(--color-tint);
  }
</style>
