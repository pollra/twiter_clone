<template>
  <button class="tweet">트윗하기</button>
</template>

<script>
  export default {
    name: "tweetBtn",

  }
</script>

<style scoped>
  button{
    top:5px;
    position: relative;
    display: block;
    padding: 7px 17px;
    border-radius: 100px;
    border: 0px;
    font-size: 11pt;
    font-weight: 600;
    color: #ffffff;
    background: #48AAE6;
    cursor: pointer;
  }
  button:hover{
    background: #1B95E0;

  }
</style>
