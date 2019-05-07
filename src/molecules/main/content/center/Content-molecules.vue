<template>
  <div class="content-component">
    <div class="content-inner">
      <div class="ci-retweet" v-if="tweetContent.userInfo.reTweet">
        <i class="fas fa-retweet"></i>
        <span>{{this.tweetContent.userInfo.reTweet}} 님이 리트윗했습니다.</span>
      </div>
      <content-icon v-bind:img-path="tweetContent.userInfo.imageIconPath" v-bind:size="iconSize.content"></content-icon>
      <div class="cc-content">
        <div class="content-user-info">
          <div class="uI-name" v-text="tweetContent.userInfo.name"></div>
          <div class="uI-id" v-text="tweetContent.userInfo.id"></div>
          <div class="middot">.</div>
          <div class="uI-time" v-text="tweetContent.contentInfo.time"></div>
        </div>
        <div class="content-text" v-text="tweetContent.contentInfo.text"></div>
        <div class="translation">
          <i class="fas fa-globe-americas"></i>
          <span>트윗 번역하기</span>
        </div>
        <content-images v-bind:images="tweetContent.contentInfo.images"></content-images>
        <div class="content-bottom-btns">
          <div>
            <i class="far fa-comment"></i>
            <span>{{tweetContent.contentInfo.bottomInfo.comment}}</span>
          </div>
          <div>
            <i class="fas fa-retweet"></i>
            <span>{{tweetContent.contentInfo.bottomInfo.reTweet}}</span>
          </div>
          <div>
            <i class="far fa-heart"></i>
            <span>{{tweetContent.contentInfo.bottomInfo.like}}</span>
          </div>
          <div>
            <i class="far fa-envelope"></i>
          </div>
        </div>
        <div class="thread-look" v-if="tweetContent.thread">
          <div class="miniLine">
            <div></div>
          </div>
          <content-icon
            class="user-icon-thread"
            v-bind:img-path="tweetContent.userInfo.imageIconPath"
            v-bind:size="iconSize.thread"></content-icon>
          <span>이 스레드 보기</span>
        </div>
        <div class="promotion-look">
          <i class="fas fa-external-link-square-alt"></i>
          <span>프로모션 중</span>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
    import ContentIcon from "../../../../atoms/icons/ContentIcon";
    import ContentImages from "../../../../atoms/images/ContentImages";
    export default {
      name: "content-molecules"
      ,
      components: {'content-images':ContentImages, 'content-icon':ContentIcon},
      data(){
        return {
          test:false,
          tweetContent:{
              userInfo:{
                reTweet:'이승근',
                imageIconPath:'/src/assets/content/user01.jpg',
                name:'간zㅣNam',
                id:'@=(\'ㅅ \'@v )'
              },
              contentInfo:{
                language:'ko',
                time:'1시간',
                images:['/src/assets/content/content02.jpg'],
                text:'실제 입력은 불가능한 화면이에욤',
                link:'',
                bottomInfo:{
                  comment:'1',
                  reTweet:'39',
                  like:'167',
                  letter:''
                }
              },
              thread:true,
              promotion:false
            },
          iconSize:{
            content:48,
            thread:28
          }
        }
      }
    }
</script>

<style scoped>
  .content-component{
    width: 100%;
    border-bottom: #e6ecf0 1px solid;
    position: relative;
  }
  .content-inner{
    padding: 10px;
    position:relative;
  }
  .ci-retweet{
    width: 100%;
    line-height: 20px;
    margin-left: 32px;
    display: flex;
    color: #66757f;
  }
  .ci-retweet > i{
    float: left;
    line-height: 22px;
    font-size: 14px;
    margin-right: 5px;
  }
  .ci-retweet > span{
    font-size: 12px;
  }
  .content-user-info{
    display: inline-flex;
  }
  .cc-content{
    margin-left: 55px;
  }
  .content-user-info > div{
    margin-right: 3px;
  }
  .uI-name{
    font-weight: bold;
    font-size: 15px;
  }
  .uI-id{
    font-size: 14px;
    color: #66757f;
  }
  .middot{
    line-height: 12px;
    margin: 0px 2px;
  }
  .uI-time{
    font-size: 14px;
    color: #66757f;
  }
  .content-text{
    font-size: 14px;
  }
  .translation{
    font-size: 12px;
    color: #66757f;
    margin: 10px 0px;
  }
  .content-bottom-btns{
    display: inline-flex;
    margin: 10px 0px;
    color: #66757f;
  }
  .content-bottom-btns > div{
    width: 80px;
    padding-top: 5px;
  }
  .content-bottom-btns > div > i{
    padding-right: 6px;
    font-size: 17px;
  }
  .content-bottom-btns > div > span{
    font-weight: bold;
    font-size: 13px;
  }
  .thread-look {
    width: 100%;
    color: #48AAE6;
    font-size: 14px;
    line-height: 30px;
  }
  .promotion-look{
    font-size: 13px;
    color: #66757f;
  }
  .promotion-look > span{
    margin-left: 5px;
  }
  .promotion-look > i{
    font-size: 14px;
  }
  .thread-look > .user-icon-thread{
    left: 20px;
  }
  .miniLine > div{
    background: black;
    border-right: 1px solid #48AAE6;
  }
  .miniLine{
    position: absolute;
    height: 100px;
    left: 10px;
    top: 82px;
    bottom: 50px;
    width: 25px;
  }
</style>
