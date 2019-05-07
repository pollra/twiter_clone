<template>
  <div id="content-component">
    <div class="content-inner">
      <div :class="{}">...님이 리트윗했습니다.</div>
    </div>
  </div>
</template>

<script>
    export default {
      name: "content-molecules"
      ,data(){
        return {
          tweetContent:{
            userInfo:{
              reTweet:'',
              imageIconPath:'',
              name:'',
              id:'@'
            },
            contentInfo:{
              time:'',
              link:'',
              text:'',
              bottomInfo:{
                comment:'',
                like:'',
                reTweet:'',
                letter:''
              }
            }
          },
        }
      }
    }
</script>

<style scoped>

</style>
