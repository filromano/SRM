<template>
  <div class="main">
    <sidebar></sidebar>
    <main-content></main-content>
  </div>
</template>

<script>
import Sidebar from './Sidebar.vue'
import MainContent from './MainContent.vue'
export default {
  components: {
    Sidebar,
    MainContent
  }
}
</script>
<style lang="scss">
  .main{
    display: block;
    width: 100%;
    height: 100%;
    float: left;
  }
</style>

