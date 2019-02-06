<template>
    <div class="main-content">
        <app-header></app-header>
        <app-dynamic-content></app-dynamic-content>
    </div>
</template>
<script>
import Header from './MainContent/Header.vue'
import DynamicContent from './MainContent/DynamicContent.vue'
export default {
    components: {
        appHeader: Header,
        appDynamicContent: DynamicContent
    }
        
}
</script>
<style lang="scss">
    .main-content{
        display: block;
        width: 82%;
        height: 100%;
        float: left;
        box-sizing: border-box;
        padding-left: 5px; 
    }
</style>
