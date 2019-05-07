<template>
  <div class="rightBoard">
    <follow-recommendation-molecules class="followRe module"></follow-recommendation-molecules>
    <footer-molecules class="footer"></footer-molecules>
  </div>
</template>

<script>
    import FollowRecommendationMolecules from "../../../molecules/main/content/left/FollowRecommendation-molecules";
    import FooterMolecules from "../../../molecules/main/content/left/Footer-molecules";
    export default {
        name: "RightBoard-oraganisms",
      components: {
        'footer-molecules':FooterMolecules,
        'follow-recommendation-molecules':FollowRecommendationMolecules,

      },
    }
</script>

<style scoped>
  .rightBoard{
    display: block;
    margin-top: 10px;
    width: 290px;
  }
  .module{
    margin-bottom: 10px;
  }
  @media (max-width: 1235px) {
    .followRe{
      display: none;
    }
    .footer{
      display: none;
    }
  }
  @media (min-width: 1236px) {
    .followRe{
      display: block;
    }
    .footer{
      display: block;
    }
  }
</style>
