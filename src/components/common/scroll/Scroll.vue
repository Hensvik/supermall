<template>
  <div class="wrapper" ref="wrapper">
    <div class="content">
      <slot></slot>
    </div>

  </div>
</template>

<script>
  import BScroll from 'better-scroll'

  export default {
    name: "Scroll",
    props:{
      probeType:{
        type:Number,
        default:0
      },
        /*pullUpLoad:{
        type:Boolean,
        default:false
      }*/
    },
    data(){
      return{
        scroll:null
      }
    },
    methods:{
      scrollTo(x,y,time=300){
        this.scroll && this.scroll.scrollTo && this.scroll.scrollTo(x,y,300)
      },

      /*finishPullUp(){
        this.scroll.finishPullUp()
      },*/

      refresh(){
        console.log('---');
        this.scroll && this.scroll.refresh()
      }
    },

    mounted(){
      this.scroll = new BScroll(document.querySelector('.wrapper'),{
        probeType:this.probeType,
        pullUpload: this.pullUpload ,
        click:true
      })

      this.scroll.on('scroll',(position) =>{
        this.$emit('scroll',position)
      })

      /*this.scroll.on('pullingUp ',()=>{
        this.$emit('pullingUp'  )
      })*/


    }
  }
</script>

<style scoped>

</style>
