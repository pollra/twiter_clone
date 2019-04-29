<template>
  <div class="trend">
    <div class="trendInner">
      <div class="trendIntro">
        <h3 class="trendTitle">나를 위한 트렌드</h3>
        <span class="middot">.</span>
        <a class="linkChange">변경하기</a>
      </div>
      <div class="prettyLink" v-for="prettyLink in prettyLinks" :key="prettyLink">
        <span class="link_name">{{prettyLink.name}}</span>
        <div class="link_context" v-text="prettyLink.context"></div>
        <div class="link_stats" v-text="prettyLink.stats"></div>
      </div>
    </div>
  </div>
</template>

<script>
    export default {
        name: "MyTrend-molecules",
      data(){
          return {
            prettyLinks:[
              {
                name: '#해산물_호불호',
                context: '',
                stats:'2,957 트윗'
              },{
                name: '정개특위',
                context: '',
                stats:'3,436 트윗'
              },{
                name: '패스트트랙 지정',
                context: '',
                stats:'6,061 트윗'
              },{
                name: '박정희 독재자',
                context: '',
                stats:''
              },{
                name: '#자캐가_00신의_신관이라면',
                context: '',
                stats:'1,163 트윗'
              },{
                name: '지정 시도',
                context: '',
                stats:'1,118 트윗'
              },{
                name: '독도수호',
                context: '',
                stats:''
              },{
                name: '서스페리',
                context: '',
                stats:''
              },{
                name: '자유당 해산',
                context: '',
                stats:'5,900 트윗'
              },{
                name: '민주당 의원들',
                context: '',
                stats:'5,320 트윗'
              }
            ]
          }
      }
    }
</script>

<style scoped>
  .trend{
    background: #ffffff;
    width: 100%;
  }
  .trendInner{
    padding: 15px;
  }
  .trendIntro{
    display: flex;
  }
  .middot{
    margin-left: 4px;
    margin-right: 3px;
    font-size: 10pt;
    line-height: 24px;
  }
  .linkChange{
    color: #1B95E0;
    font-size: 10pt;
    line-height: 28px;
  }
  .prettyLink{
    margin: 5px 0px;
  }
  .prettyLink > .link_name{
    color: #1B95E0;
    font-weight: bold;
    font-size: 11pt;
  }
  .prettyLink > .link_context{
    font-size: 10pt;
    color: #657786;
  }
  .prettyLink > .link_stats{
    font-size: 10pt;
    line-height: 15px;
    color: #657786;
  }
</style>
