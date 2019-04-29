<template>
  <div id="top-template">
    <div class="top-template">
      <top-organisms></top-organisms>
    </div>
  </div>
</template>

<script>
    import TopOrganisms from "../../organisms/main/top/Top-Organisms";
    export default {
        name: "Top-Template",
      components: {'top-organisms':TopOrganisms}
    }
</script>

<style scoped>
  #top-template{
    background: #ffffff;
    position: fixed;
    top:0px;
    left: 0px;
    right: 0px;
    width: 100%;
    height: 46px;
    margin: 0px;
    padding: 0px;
    /*box-shadow: 0px -16px 10px 10px black;*/
    z-index: 10;
    line-height: 20px;
    border-bottom: 1px solid rgba(0,0,0,0.25);
    box-sizing: border-box;
  }
  .top-template{
    width: 100%;
    height: 46px;
    border-bottom: 1px solid rgba(0,0,0,0.05);
    box-sizing: content-box;
  }
</style>
