<template>
    <i v-bind:class="getIconCategory()"></i>
  <!--<i class="fas fa-home"></i>-->
  <!--<i class="far fa-bell"></i>-->
  <!--    <i class="far fa-envelope"></i>-->
</template>

<script>
  export default {
    data(){
      return {
        icon:'fas'
      }
    },
    props:['iconCategory'],
    methods:{
      getIconCategory(){
        let result = '';
        if(this.iconCategory === 'home') {
          result = 'fas fa-home'
        }else if(this.iconCategory === 'bell' || this.iconCategory==='envelope'){
          result = 'far fa-'+ this.iconCategory;
        }
        return result;
      }
    }
  }
</script>

<style scoped>
  i {
    margin: 0px;
    padding: 0px;
  }
  @media (max-width: 935px) {
    /* 왼쪽 버튼의 UI 설명이 사라짐.*/
  }
</style>
