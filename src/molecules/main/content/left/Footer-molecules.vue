<template>
  <div class="footer">
    <div class="footer-content">
      <span class="footer-content-title">ⓒ 2019 Twitter</span>
      <span v-for="item in footerButtons" class="footer-content-item" :rel="item.link">{{item.name}}</span>
    </div>
    <div class="footer-bottom">
      <i class="fas fa-external-link-alt"></i>
      <span class="footer-bottom-item">트위터로 광고하새오</span>
    </div>
  </div>
</template>

<script>
    export default {
        name: "Footer-molecules",
      data(){
        return {
          footerButtons:[
            {
              name:'회사소개',
              link:''
            },{
              name:'고객센터',
              link:''
            },{
              name:'이용약관',
              link:''
            },{
              name:'개인정보 처리방침',
              link:''
            },{
              name:'쿠키',
              link:''
            },{
              name:'광고 정보',
              link:''
            },{
              name:'브랜드',
              link:''
            },{
              name:'블로그',
              link:''
            },{
              name:'시스템 현황',
              link:''
            },{
              name:'애플리케이션',
              link:''
            },{
              name:'인재채용',
              link:''
            },{
              name:'마케팅',
              link:''
            },{
              name:'비즈니스',
              link:''
            },{
              name:'개발자',
              link:''
            },
          ]
        }
      }

    }
</script>

<style scoped>
  .footer{
    background: #ffffff;
  }
  .footer-bottom{
    border-top: 1px solid #e6ecf0;
  }
  .footer-content{
    padding: 15px;
    font-size: 12px;
    color: #657786;
    display: block;
  }
  .footer-content-item{
    margin: 3px;
    display: inline-block;
    line-height: 15px;
  }
  .footer-content-item:hover{
    color: #1B95E0;
    text-decoration: underline;
    cursor: pointer;
  }
  .footer-bottom{
    padding: 15px;
    font-size: 12px;
    color: #1B95E0;
  }
  .footer-bottom-item:hover{
    text-decoration: underline;
    cursor: pointer;
  }
</style>
