<template>
  <div class="userImage">
    <img src="/src/assets/TT.jpg">
  </div>
</template>

<script>
    export default {
        name: "UserIcon"
    }
</script>

<style scoped>
  .userImage{
    position: relative;
    float: left;
    top: 7px;
    border: 0px solid #ffffff;
    margin-right: 20px;
    cursor:pointer;
  }
  img{
    width: 31px;
    border-radius: 16px;
  }

</style>
