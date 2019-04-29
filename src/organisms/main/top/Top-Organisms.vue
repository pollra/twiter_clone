<template>
    <div id="top-organisms">
      <leftContainer></leftContainer>
      <img src="../../../assets/Twitter_icon.png">
      <rightContainer></rightContainer>
    </div>
</template>

<script>
  import LeftContainer from '../../../molecules/main/top/LeftContainer-molecules';
  import RightContainer from '../../../molecules/main/top/RightContainer-molecules';
    export default {
      components:{
        'leftContainer':LeftContainer,
        'rightContainer':RightContainer
      }
    }
</script>
<!--936 이하에서는 왼쪽 위의 버튼이 사라지고 트위터 검색하기 입력이 짧아짐. flex 는 좌우로 고정됨-->
<style scoped>
  #top-organisms{
    /*background: cornflowerblue;*/
    max-width: 1190px;
    width: auto;
    min-width: 605px;
    text-align: center;
    position: relative;
    height: 100%;
    margin:0px auto;
  }
  img{
    padding: 0px;
    position: absolute;
    width: 21px;
    margin: 14px 0 0 0;
    line-height: 20px;
    cursor: pointer;
    /*transition: all .2s;*/
  }
  /* min-width: 500px : 500px 이상의 화면 범위에서만 작동.*/
  /* max-width: 600px : 600px 이하의 화면 범위에서만 작동.*/
  /*@media (min-width: 500px) and (max-width: 600px) {*/
  @media (max-width: 600px) { /*600 이하*/
    img {
      width: 18px;
      margin-top: 13px;
      transition: all .2s;
    }
    #top-organisms{
      /*background: cornflowerblue;*/
      width: 600px;
      text-align: center;
      position: relative;
      height: 100%;
      margin:0px auto;
    }
  }
  @media (max-width: 935px) { /* 935 이하 ~*/
    /* 왼쪽 버튼의 UI 설명이 사라짐.*/
    #top-organisms{
    }
  }
  @media (max-width: 1235px) { /* 1235 이하 ~*/
  /*  top-organisms : 890*/
    #top-organisms{
      max-width: 890px;
    }
    img{
      left: 43%;
    }
  }
  @media (min-width: 1236px) { /* 1236 이상 ~*/
    /*  top-organisms : 넓이 1190*/
    #top-organisms{
      max-width: 1190px;
    }
    img{
      left: 50%;
    }
  }
</style>
