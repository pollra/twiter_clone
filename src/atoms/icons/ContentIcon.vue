<template>
  <div id="contentIcon" :style="getSize">
    <img :src="imgPath">
  </div>
</template>

<script>
    export default {
        name: "ContentIcon",
      props:['imgPath', 'size'],
      computed:{
        getSize(){
          return `width:${this.size}px;height:${this.size}px;`
        }
      }
    }
</script>

<style scoped>
  img{
    width: auto;
    height: 100%;
  }
  #contentIcon{
    border-radius: 50%;
    overflow: hidden;
    position: absolute;
  }
</style>
