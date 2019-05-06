<template>
  <div class="mainInput">
    <div class="mI-Inner">
      <user-icon class="mI-userIcon"></user-icon>
      <div class="mI-formOut">
        <form class="mI-form">
          <div class="mI-input-box" @click="openTweet">
            <div id="mI-input-input">
              <div>{{this.placeholder}}</div>
              <i class="fas fa-image"></i>
            </div>
          </div>
          <div id="mI-form-box" class="disnone">
            <div id="mI-input-area">
              <textarea id="mI-area" @keyup="resize" :placeholder="this.placeholder" @focusout="closeTweet">
              </textarea>
            </div>
            <div id="mI-buttons-out">
              <div id="mI-icon-box">
                <div class="icon-image mI-icon">
                  <i class="fas fa-image"></i>
                </div>
                <div class="icon-plus mI-icon">
                  <i class="far fa-plus-square"></i>
                </div>
                <div class="icon-booth mI-icon">
                  <i class="fas fa-person-booth"></i>
                </div>
                <div class="icon-marker mI-icon">
                  <i class="fas fa-map-marker-alt"></i>
                </div>
              </div>
              <div id="mI-submit-box">
                <div class="submit-plus mI-icon">
                  <i class="fas fa-plus-circle"></i>
                </div>
                <div class="submit-button">
                  <tweet-btn class="mI-tweet"></tweet-btn>
                </div>
              </div>
            </div>
          </div>
        </form>
      </div>
    </div>
  </div>
</template>

<script>
    import UserIcon from "../../../../atoms/icons/UserIcon";
    import TweetBtn from "../../../../atoms/buttons/tweetBtn";
    export default {
      data(){
        return {
          placeholder:'무슨 일이 일어나고 있나요?'
        }
      },
      name: "InputForm-molecules",
      components: {'tweet-btn':TweetBtn, 'user-icon':UserIcon},
      methods:{
        openTweet(){
          document.getElementById('mI-input-input').classList.add('disnone');
          document.getElementById('mI-form-box').classList.remove('disnone');
          document.getElementById('mI-input-area').children.item(0).focus();
        },
        closeTweet(){
          let area = document.getElementById('mI-input-area').children.item(0);
          if(area.value.trim() === "") {
            document.getElementById('mI-form-box').classList.add('disnone');
            document.getElementById('mI-input-input').classList.remove('disnone');
            document.getElementById('mI-area').style.height = '80px';
          }
        },
        resize(){
          document.getElementById('mI-area').style.height='76px';
          document.getElementById('mI-area').style.height = document.getElementById('mI-area').scrollHeight + 'px';
        }
      }
    }
</script>

<style scoped>
  .mainInput{
    width: 100%;
    background: #E8F4FB;
    border-bottom: 1px solid #e6ecf0;
  }
  .mI-Inner{
    padding: 10px;
    position: relative;
    min-height: 30px;
  }
  #mI-icon-box{
  }
  #mI-submit-box{
  }
  .disnone{
    display: none;
  }
  .mI-formOut{
    margin-left: 55px;
    margin-right: 5px;
  }
  .mI-userIcon{
    position: absolute;
    left: 25px;
    top:13px;
  }
  .mI-input-box{
    width: 100%;
  }
  #mI-input-input{
    width: 100%;
    border: 1px solid #c6e4f7;
    border-radius: 8px;
    min-height: 36px;
    max-height: 36px;
    font-size: 14px;
    background: white;
    position: relative;
  }
  #mI-input-input > div{
    color: #1B95E0;
    margin-top: 8px;
    margin-left: 9px;
    cursor: text;
  }
  #mI-input-input > i{
    font-size: 20px;
    position: absolute;
    right: 13px;
    top:9px;
    color: #48AAE6;
  }
  #mI-input-area{
    padding: 0px;
    position: relative;
    border-radius: 7px;
    border: 2px solid rgba(27, 149, 224, 0.4);
    min-width: 500px;
    background: #ffffff;
    min-height: 80px;
  }
  #mI-input-area > textarea::placeholder{
    color: #aab8c2;
  }
  #mI-input-area > textarea{
    width: 480px;
    padding: 8px;
    border: 0px;
    background: none;
    resize: none;
    outline: none;
    overflow-y: hidden;
    min-height: 80px;
  }
  #mI-icon-box{
    position: relative;
    display: flex;

  }
  .mI-icon{
    margin: 2px;
    font-size: 25px;
    width: 45px;
    text-align: center;
    color: rgba(27, 149, 224, 0.8);
    padding: 5px;
  }
  .mI-icon:hover{
    border-radius: 5px;
    border: 1px solid rgba(27, 149, 224, 0.4);
    background: linear-gradient(to bottom, #E8F4FB, rgba(27, 149, 224, 0.1));
    padding: 4px;
  }
  #mI-icon-box{
    margin: 4px 0px;
    float: left;
    display: flex;
    flex-direction: inherit;
  }
  #mI-submit-box{
    margin: 4px 0px;
    float: right;
    display: flex;
    position: absolute;
    right: 15px;
  }
  #mI-buttons-out{
    margin: 1px 0px;
    width: 100%;
    display: flex;
  }
</style>
