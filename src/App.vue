<template>
  <div class="page">
    <main--page></main--page>
  </div>
</template>

<script>
import MainPage from "./page/Main-Page";
import WelcomePage from "./page/Welcome-Page";

export default {
  components: {'welcome--page':WelcomePage, 'main--page':MainPage},
  data(){
    return {
    }
  }
}
</script>

<style>
</style>
