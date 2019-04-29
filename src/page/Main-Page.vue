<template>
  <div class="mainPage">
    <top--template></top--template>
    <content--template></content--template>
  </div>
</template>

<script>
  import TopTemplate from "../template/main/Top-Template";
  import ContentTemplate from "../template/main/Content-Template";

  export default {
    components: {'content--template':ContentTemplate, 'top--template':TopTemplate}
  }
</script>

<style scoped>
  .mainPage{
    background: #e6ecf0;

  }
</style>
