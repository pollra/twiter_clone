<template>
  <div>
    <div class="one-img-out" v-if="images.length===1" :key="images">
      <div class="one-img-inner">
        <img class="one-img" :src="images[0]" >
      </div>
    </div>
    <div v-else="images.length >= 2">
      ㅇㅂㅇ
    </div>
  </div>
</template>

<script>
    export default {
        name: "ContentImages"
      ,props:['images'],
      created(){

      }
    }
</script>

<style scoped>
  .one-img-out{
    max-width: 506px;
    min-width: 180px;
    width: auto;
    max-height: 506px;
    height: auto;
    min-height: 180px;
    overflow: hidden;
    border-radius: 15px;
    border: 1px solid rgba(0,0,0,0.1);
    position: relative;
  }
  .one-img-inner{
    height: 100%;
    width: 100%;
  }
  .one-img.wid{
    width: 100%;
    height: auto;
    position:absolute;
    top: 0;
  }
</style>
