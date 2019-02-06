<template>
    <div class="sidebar">
        <div class="search">
            <input type="text" placeholder="Pesquise aqui">
        </div>
        <div class="sidebar-menu">
            <ul class="sidebar-list">
                <li v-for="(item, index) in menu" :key=index>{{ item.name }}</li>
            </ul>
        </div>
    </div>
</template>
<script>
export default {
    data(){
        return{
            menu: [
                {
                    name: 'Painel de Gestão',
                    link: '#'
                },
                {
                    name: 'Conta Digital',
                    link: '#'
                },
                {
                    name: 'Ant. de Recebiveis',
                    link: '#'
                }
            ]
        }
    }
}
</script>
<style lang="scss">
    @import '../assets/css/helper.scss';
    .sidebar{
        display: block;
        width: 18%;
        height: 100%;
        float: left;
    }
    .search{
        display: block;
        position: relative;
        width: 100%;
        height: $headerHeight;
        background: white;
        input{       
            box-sizing: border-box;
            width: calc(100% - 35px);
            height: 100%;
            border: none;
            font-size: 18px;
            text-align: right;
            padding: 10px;
            outline: none !important;
        }
        &::after{
                display: block;
                content: '';
                position: absolute;
                right: 0;
                top: 15px;
                width: 30px;
                height: 30px;
                background-image: url('../assets/magnify.png');
                background-size: cover;
            }
    }
    .sidebar-menu{
        display: block;
        width: 100%;
        height: calc(100% - 60px);
        background: $darkblue;
        color: white;
    }
    .sidebar-list{
        list-style: none;
        li{
            border-bottom: 1px solid $lightblue;
            position: relative;
            padding: 20px 10px 20px 40px;
            font-size: 16px;
            cursor: pointer;
            &:before{
                display: block;
                position: absolute;
                left: 5px;
                top: 15px;
                content: '';
                width: 30px;
                height: 30px;
                background-image: url('./../assets/planet.png');
                background-size: cover; 
            }
            &:hover{
                background: $lightblue;
            }
        }
    }
</style>
