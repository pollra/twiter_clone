<!--Content-Template-->
<template>
  <div class="leftBoard">
    <name-card-molecules id="nameCard" class="module"></name-card-molecules>
    <my-trend-molecules id="myTrend" class="module"></my-trend-molecules>
    <follow-recommendation-molecules id="followRe" class="module"></follow-recommendation-molecules>
    <footer-molecules id="footer"></footer-molecules>
  </div>
</template>

<script>
    import NameCardMolecules from "../../../molecules/main/content/left/NameCard-molecules";
    import MyTrendMolecules from "../../../molecules/main/content/left/MyTrend-molecules";
    import FollowRecommendationMolecules from "../../../molecules/main/content/left/FollowRecommendation-molecules";
    import FooterMolecules from "../../../molecules/main/content/left/Footer-molecules";
    export default {
      name: "LeftBoard-Oragaisms",
      components: {
        'footer-molecules':FooterMolecules,
        'follow-recommendation-molecules':FollowRecommendationMolecules, 'my-trend-molecules':MyTrendMolecules, 'name-card-molecules':NameCardMolecules}
    }
</script>
<!--935 이하는 마진 10-->
<style scoped>
  .leftBoard{
    display: block;
    margin-top: 10px;
    float: left;
    width: 290px;
  }
  .module{
    margin-bottom: 10px;
  }
</style>
