<template>
    <div class="header">
        <div class="logo">
            <h1>Logo</h1>
        </div>
        <div class="user">
            <div class="user-name">
                <span>Sandra Oliveira</span>
            </div>
            <div class="notifications">
                <img src="../../assets/bell.png" width="24" height="24" alt="">
                <span class="notification-number">5</span>
            </div>
        </div>
        <div class="economic-group">
            <span>Grupo Ecônomico:</span>
            <select class="visions" name="visions">
                <option value="Visão Agregada 1">Visão Agregada 1</option>
                <option value="Visão Agregada 2">Visão Agregada 2</option>
                <option value="Visão Agregada 3">Visão Agregada 3</option>
            </select>
        </div>
    </div>
</template>
<style lang="scss">
    @import '../../assets/css/helper.scss';
    .header{
        display: block;
        height: $headerHeight;
        width: 100%;
        float: left;
        box-sizing: border-box;
        background: white;
        padding: 10px;
    }
    .logo{
        float: left;
    }
    .user{
        display: block;
        position: relative;
        box-sizing: border-box;
        height: 38px;
        float: right;
        background: $darkblue;
        padding-left: 40px;
        cursor: pointer;
        &::before{
            display: block;
            position: absolute;
            content: '';
            width: 38px;
            height: 38px;
            background-image: url('../../assets/profile.png');
            background-size: cover;
            left: 0;
            

        }
    }
    .user-name{
        display: block;
        box-sizing: border-box;
        float: left;
        background: $darkblue;
        padding: 10px;
        color: white;
    }
    .notifications{
        display: block;
        position: relative;
        float: right;
        width: 38px;
        height: 38px;
        background: $lightblue;
        img{
            display: block;
            margin: auto;
            padding-top: 8px;
        }
    }
    .notification-number{
        display: block;
        position: absolute;
        box-sizing: border-box;
        background: red;
        color: white;
        width: 20px;
        height: 20px;
        padding: 3px 0 0 6px;
        border-radius: 50%;
        top: 2px;
        right: 2px;
        font-size: 12px;
    }
    .economic-group{
        display: block;
        float: right;
        margin: 10px 20px 0 0;
        span{
            font-size: 18px;
            float: left;
            margin: 3px 10px 0 0;
        }
    }
    .visions{
        font-size: 18px;
    }
</style>

