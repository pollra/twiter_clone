<template>
  <div class="followRecommendation">
    <div class="fR-inner">
      <div class="fR-info">
        <h3 class="fR-info-title">팔로우 추천</h3>
        <span class="middot">.</span>
        <div class="fR-info-btn">새로 고침</div>
        <span class="middot">.</span>
        <div class="fR-info-btn">모두 보기</div>
      </div>
      <div class="fR-items">
        <div class="fR-item" v-bind:class="{tM:index >= 1 ? true : false}" v-for="(item, index) in frItems" :key="item">
          <a class="item-img">
            <img v-bind:src="item.imgPath">
          </a>
          <div class="item-close">
            <i class="fas fa-times"></i>
          </div>
          <div class="fR-item-content">
            <div class="fR-item-userText">
              <div class="item-name">
                <span>{{item.name}}</span>
              </div>
              <div class="item-link">
                <span>{{item.linkName}}</span>
              </div>
            </div>
            <button class="item-follow-btn">팔로우</button>
          </div>
        </div>
      </div>
    </div>
    <div class="fR-find">
      <div class="fR-find-inner">
        <i class="fas fa-user-friends"></i>
        <span>지인들을 찾아보세요</span>
      </div>
    </div>
  </div>
</template>

<script>
    export default {
      name: "FollowRecommendation-molecules",
      data(){
        return {
          frItems:[
            {
              name:'집사를찾습니다',
              imgPath:'/src/assets/follow/follow01.png',
              linkName: '@참치다떨어졌다'
            },{
              name:'이렇게_반으로_쪼개버릴거야_시발',
              imgPath:'/src/assets/follow/follow02.jpg',
              linkName: '@sibal'
            },{
              name:'단비꺼야',
              imgPath:'/src/assets/follow/follow03.jpg',
              linkName: '@너그거맛있어보이네?'
            }
          ]
        }
      }
    }
</script>

<style scoped>
  .followRecommendation{
    width: 100%;
    overflow: hidden;
    background: white;
    display: block;
  }
  .fR-inner{
    padding: 15px 15px 0px 15px;
  }
  .fR-info{
    display: flex;
    line-height: 25px;
    margin-bottom: 10px;
  }
  .middot{
    font-size: 10pt;
    margin-left: 3px;
    margin-right: 3px;
    line-height: 23px;
  }
  .fR-info-btn{
    font-size: 12px;
    line-height: 30px;
    color: #1B95E0;
  }
  .item-img > img{
    width: 48px;
    height: 48px;
    border-radius: 50%;
    position: absolute;
  }
  .fR-item-userText{
    display: flex;
    overflow: hidden;
    text-overflow: ellipsis;
    white-space: nowrap;
  }
  .fR-item-content{
    margin-left: 58px;
    margin-right: 20px;
  }
  .item-name{
    font-size: 14px;
    font-weight: bold;
  }
  .fR-items{
    min-height: 48px;
    font-size: 12px;

  }
  .item-follow-btn{
    display: block;
    width: 100px;
    border-radius: 15px;
    height: 30px;
    border: 1px solid #1B95E0;
    background: white;
    color: #1B95E0;
    font-weight: bold;
    margin-top: 5px;
  }
  .fR-item{
    /*width: 100%;*/
    padding-bottom: 8px;
    border-bottom: 1px solid #e6ecf0;
  }
  .item-link{
    font-size: 12px;
    color: #657786;
    margin-left: 3px;
  }
  .item-close{
    position: relative;
    display: inline-block;
    color: #ccd6dd;
    float: right;
    margin-left: 10px;
    background: #ffffff;
  }
  .tM{
    margin-top: 10px;
  }
  .fR-find{
    border-top:1px solid #e6ecf0;
    margin-top: -1px;
    padding: 15px;
    font-size: 14px;
    color: #1B95E0;
  }
  .fR-find-inner{
    font-size: 12px;
  }
</style>
