<template>
  <div class="btnContainer">
    <div class="btn"
         v-for="(btnInfo, index) in buttons"
         :key="btnInfo"
         :id="btnInfo[0]+'-btn'"
         v-bind:class="{actived:btnInfo[2]}"
         v-on:click="btnActived(index)">
      <Icons class="icon" v-bind:iconCategory="btnInfo[0]"></Icons>
      <span v-text="btnInfo[1]"></span>
    </div>
  </div>
</template>

<script>
  import Icons from '../../../atoms/icons/NavIcon'
  export default {
    data(){
      return {
        buttons:[
          ['home','홈',true],
          ['bell','알림',false],
          ['envelope','쪽지',false]
        ],
      }
    },
    components:{
      'Icons':Icons
    },
    methods:{
      btnActived(btnNumber){
        console.log("버튼 눌림. 이벤트 작동 "+btnNumber);
        for(let i=0; i<this.buttons.length; i++) {
          if(i !== btnNumber){
            document.getElementById(`${this.buttons[i][0]}-btn`).classList.remove('actived');
          }else if(i === btnNumber){
            document.getElementById(`${this.buttons[i][0]}-btn`).classList.add('actived');
          }
        }
      }
    },
  }
</script>

<style scoped>
  span{
    line-height: 35px;
    font-size: 10pt;
    font-weight: 700;
    outline: none;
    border: 0px;
    background: white;
    margin: 0 0 0 5px;
    color: #66757f;
  }
  .btn{
    float: left;
    margin: 0px;
    cursor: pointer;
    display: flex;
    padding: 5px 15px 4px 15px;
  }
  .icon{
    line-height: 35px;
    margin: 0px;
    font-size: 15pt;
    color: #66757f;
  }
  .actived {
    color:#1B95E0;
    border-bottom: solid 2px #1B95E0;
  }
  .actived span, .actived .icon{
    color:#1B95E0;
  }

  .btn:hover > .icon, .btn:hover > span{
    color: #1B95E0;
  }
  .btn:hover{
    transition: .1s;
    border-bottom: solid 2px #1B95E0;
  }

  @media (max-width: 935px) {
    /* 왼쪽 버튼의 UI 설명이 사라짐.*/
    span{
      display: none;
    }
    .btn{
      margin: 0px;
      padding: 5px 15px 4px 15px;
    }
  }
  .btnContainer{
    float: left;
  }
  @media (min-width: 936px) and (max-width: 1234px) { /* 936 이상 ~ 1234 이하*/
    .btnContainer{
      margin-left:0px;
      margin-right:0px;
    }
  }
</style>
