<!--LeftBoard-organisms-->
<template>
  <div class="nameCard">
    <div class="nameCardTitleImage">
      <img>
    </div>
    <div class="nameCardInfo">
      <a>
        <img class="nameCardUserImage" src="/src/assets/TT.jpg">
      </a>
      <div class="nameCardInfoUser">
        <div>
          <span class="nicName">{{nikName}}</span>
        </div>
        <div>
          <span class="linkName">{{linkName}}</span>
        </div>
      </div>
      <div class="nameCardTweet">
        <ul>
          <li>
            <div class="follow">트윗</div>
            <div class="followNum">ㅠㅠ</div>
          </li>
          <li>
            <div class="follow">팔로잉</div>
            <div class="followNum">ㅠㅠ</div>
          </li>
          <li>
            <div class="follow">팔로워</div>
            <div class="followNum">ㅠㅠ</div>
          </li>
        </ul>
      </div>
    </div>
  </div>
</template>

<script>
    export default {
        name: "NameCard-molecules",
      data(){
        return {
          nikName: '너무 슬픈 개구리',
          linkName:'@Pollra'
        }
      }
    }
</script>

<!--214 x 290-->
<style scoped>
  div, ul, li, span, a{
    margin: 0px;
    padding: 0px;
  }
  .nameCard{
    width: 290px;
    height: 214px;
    background: white;
    line-height: 20px;
  }
  .nameCardTitleImage{
    background: #1B95E0;
    height: 95px;
    width: 100%;
  }
  .nameCardInfo{
    height: 118px;
    width: 100%;
  }
  .nameCardInfo a{
    display: inline-block!important;
    max-width: 100%;
    background-color: #fff;
    border-radius: 50%;
    margin: -30px 0 0 8px;
    padding: 1px;
    vertical-align: bottom;
  }
  .nameCardUserImage{
    border-radius: 50%;
    height: 72px;
    width: 72px;
    border: 2px solid #fff;
    -moz-box-sizing: border-box;
    box-sizing: border-box;
    color: #fff;
  }
  .nameCardInfoUser{
    position: absolute;
    top: 110px;
    left: 90px;
    width: 185px;
  }

  .nicName{
    font-size: 13pt;
    font-weight: bold;
    line-height: 24px;
  }
  .linkName{
    font-size: 10.5pt;
    color: #657786;
  }
  .nameCardTweet{
    display: block;
    padding-left: 16px;
    padding-right: 16px;
    padding-bottom: 16px;
  }
  .nameCardInfo .nameCardTweet{
    padding-top: 16px;
  }
  .nameCardTweet > ul{
    list-style: none;
    display: table;
    table-layout: fixed;
    min-width: 100%;
  }
  .nameCardTweet > ul > li {
    display: table-cell;
    padding: 0px;
    box-sizing: border-box;
    overflow: hidden;
    text-align: inherit;
    transition: all .15s ease-in-out;
    font-size: 14px;
    width: 1px;
  }
  .nameCardTweet .follow{
    color: #657786;
    font-size: 12px;
    font-weight: bold;
    line-height: 16px;
    overflow: hidden;
    transition: all .15s ease-in-out;
  }
  .nameCardTweet .followNum{
    display: block;
    font-size: 18px;
    font-weight: bold;
    padding-top: 3px;
    color:#1B95E0;
    line-height: 1;
  }

</style>
