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
    border: 0px solid #ffffff;
    cursor:pointer;
  }
  img{
    width: 31px;
    border-radius: 16px;
  }

</style>
