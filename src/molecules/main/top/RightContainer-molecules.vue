<template>
  <div class="rightContainer">
    <form>
      <input placeholder="트위터 검색하기" @click="searchClickEvent">
      <i class="fas fa-search"></i>
    </form>
    <user-icon class="rC-userIcon"></user-icon>
    <tweetBtn></tweetBtn>
  </div>
</template>

<script>
    import UserIcon from "../../../atoms/icons/UserIcon";
    import TweetBtn from "../../../atoms/buttons/tweetBtn";
    export default {
        name: "RightContainer-molecules",
      components: {'user-icon':UserIcon, 'tweetBtn':TweetBtn},
      methods:{
        searchClickEvent(){

        }
      }
    }
</script>

<style scoped>
  input{
    border-radius: 21px;
    border: 1px solid #e6ecf0;
    padding: 8px 32px 8px 12px;
    display: block;
    line-height: 16px;
    background-color:#f5f8fa;
    outline-style: none;
    transition: all 0.2s ease-in;
    box-sizing: border-box;
    position: relative;
    width: 100%;
    font-size: 9pt;
  }
  input:focus{
    border: 2px solid #1B95E0;
    padding: 7px 30px 7px 11px;
    background: #fff;
  }
  .rightContainer{
    float: right;
    text-align: left;
    height: 100%;
  }
  i{
    position: absolute;
    top: 8px;
    right: 8px;
    width: 26px;
    height: 26px;
    display: block;
    font-size: 13pt;
    color: #66757f;
  }
  form{
    margin: 6px 15px 0 0;
    width: 221px;
    height: 33px;
    float: left;
    font-size: 12pt;
    position: relative;
    display: block;
    box-sizing: border-box;
  }
  @media (max-width: 936px) and (min-width: 701px){
    form{
      width: 140px;
    }
  }
  @media (max-width: 700px) {
    form{
      width: 94px;
    }
  }
  .rC-userIcon{
    top: 7px;
    float: left;
    margin-right: 20px;
  }
</style>
