<template>
  <div id="app">
    <router-view></router-view>
    <app-tab-bar/>
  </div>
</template>

<script>
import AppTabBar from './components/content/tabbar/AppTabBar'
export default {
  components: { AppTabBar },
  
}
</script>

<style>
  @import "./assets/css/base.css";
</style>
