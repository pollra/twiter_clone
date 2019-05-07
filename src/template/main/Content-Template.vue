<template>
  <div id="content-template">
    <left-board-oragaisms id="leftBoard"></left-board-oragaisms>
    <main-oraganisms id="mainBoard"></main-oraganisms>
    <right-board-oraganisms></right-board-oraganisms>
  </div>
</template>

<script>
    import LeftBoardOragaisms from "../../organisms/main/content/LeftBoard-organisms";
    import MainOraganisms from "../../organisms/main/content/Main-organisms";
    import RightBoardOraganisms from "../../organisms/main/content/RightBoard-organisms";
    export default {
        name: "Content-Template",
      components: {'left-board-oragaisms':LeftBoardOragaisms, 'main-oraganisms':MainOraganisms, 'right-board-oraganisms':RightBoardOraganisms}
    }
</script>

<style scoped>
  #content-template{
    /*height: 2000px;*/
    min-width: 890px;
    max-width: 1190px;
    position: relative;
    display: flex;
    margin: 0px auto;
    /*padding: 56px 14px 15px;*/
    padding: 0px;
    top: 46px;
    left: 0px;
  }
  #mainBoard{
    margin: 10px;
  }

/*  1235 이상이면 1190 */
  @media (min-width: 1235px) {
    #content-template{
      width: 1190px;
    }
  }
  @media (max-width: 1234px) {
    #content-template{
      width: 890px;
    }
  }
  @media (max-width: 935px) {
    #leftBoard{
      margin-left: 10px;
    }
  }
</style>
