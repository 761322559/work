<template>
  <div class="main">
    <div class="home-header">
      <img src="../assets/miaov.png" alt="">
      <div class="portrait" :class={portraitLogin:isLogin}>
        <router-link  v-if="!isLogin" :to="{name:'login'}" tag="span">登录</router-link>
        <img  v-if="isLogin" src="../assets/portrait.png" alt="">
      </div>

    </div>
    <div class="phrase">
      一起学习Vue-router
    </div>
    <div class="btns">
      <router-link :to="{name:'project'}" tag="div" class=" trans" replace>我的项目</router-link>
      <router-link :to="{name:'doc'}" tag="div" class=" trans">我的文档</router-link>
    </div>
  </div>
</template>

<script>
  export default {
    name: 'home',
    data () {
      return {
        isLogin: false
      }
    }
  }
</script>
<style>

</style>
