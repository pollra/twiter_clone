<template>
  <div class="mainBoard">
    <input-form-molecules id="main-inputForm"></input-form-molecules>

  </div>
</template>

<script>
    import InputFormMolecules from "../../../molecules/main/content/center/InputForm-molecules";
    export default {
        name: "Main-oraganisms",
      components: {'input-form-molecules':InputFormMolecules}
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
