<template>
  <div class="mainBoard">
    <input-form-molecules id="main-inputForm"></input-form-molecules>
    <content-molecules></content-molecules>
  </div>
</template>

<script>
    import InputFormMolecules from "../../../molecules/main/content/center/InputForm-molecules";
    import ContentMolecules from "../../../molecules/main/content/center/Content-molecules";
    export default {
        name: "Main-oraganisms",
      components: {'content-molecules':ContentMolecules, 'input-form-molecules':InputFormMolecules}
    }
</script>

<style scoped>
  .mainBoard{
    background: white;
    width: 590px;
  }
  #main-inputForm{

  }
</style>
