<template>
    <div class="dynamic-content">
        <div class="breadcrumbs">
            <p><span>Pagina inicial</span><span>></span><span>Painel de Gestão</span></p>
        </div>
        <div class="row dynamic-content-title">
            <div class="content-title">
                <img src="@/assets/planet-black.png" width="64" height="64" alt="">
                <h1>Painel de Gestão</h1>   
            </div>
            <div class="product">
                <span>Produto:</span>
                <select class="products-list" name="products-list">
                    <option value="Todos">Todos</option>
                    <option value="Produto 1">Produto 1</option>
                    <option value="Produto 2">Produto 2</option>
                </select>
            </div>
        </div>
        <div class="row bottom-content">
            <div class="shortcuts">
                <div class="box-title">
                    <p>Atalhos</p>
                </div>
                <div class="row">
                    <div class="operational">
                        <span>Operacional</span>
                        <div class="buttons-operational">
                            <button>Envio</button>
                            <button>Assinatura</button>
                            <button>Envio de Duplicatas</button>
                            <button>Assinatura Digital</button>
                            <button>Nova Operação</button>
                        </div>
                    </div>
                    <div class="general">
                        <span>Geral</span>
                        <div class="buttons-general">
                            <button>Carteira</button>
                            <button>Instruções</button>
                        </div>
                    </div>
                </div>
            </div>
            <div class="alerts">
                <div class="box-title">
                    <p class="alert-text">Alertas</p>
                    <span class="last-days">Últimos 5 dias</span>
                </div>
                <div class="alert-content">
                    <ul class="alert-list">
                        <li>
                            <span>23 Notas Canceladas</span>
                        </li>
                        <li>
                            <span>13 Notas canceladas</span>
                            <select class="actions-list" name="actions-list">
                                <option value="Ações">Ações</option>
                                <option v-for="(action, index) in actions" value=index :key="index">{{ action.name }}</option>
                            </select>
                        </li>
                        <li>
                            <span>7 Assinaturas Digital</span>
                            <select class="actions-list" name="actions-list">
                                <option value="Ações">Ações</option>
                                <option v-for="(action, index) in actions" value=index :key="index">{{ action.name }}</option>
                            </select>
                        </li>
                    </ul>
                </div>
            </div>
        </div>
    </div>
</template>
<script>
export default {
    data(){
        return{
            actions: [
                {
                    name: 'Deletar'
                },
                {
                    name: 'Arquivar'
                },
                {
                    name: 'Editar'
                },
                {
                    name: 'Visualizar'
                }
            ]
        }
    }
}
</script>

<style lang="scss">
    @import '../../assets/css/helper.scss';
    .dynamic-content{
        display: block;
        box-sizing: border-box;
        width: 100%;
        height: calc(100% - 80px);
        float: left;
        padding: 10px;
    }
    .breadcrumbs{
        display: block;
        width: 100%;
        height: 20px;
        span{
            margin-right: 10px;
        }
    }
    .row{
        display: block;
        width: 100%;
    }
    .dynamic-content-title{
        height: 100px;
        padding-top: 30px;
    }
    .content-title{
        display: block;
        width: 60%;
        float: left;
        h1{
            display: block;
            float: left;
            font-size: 36px;
            margin: 10px 0 0 10px;
        }
        img{
            float: left;
        }
    }
    .product{
        display: block;
        box-sizing: border-box;
        float: right;
        padding-top: 20px;
        span{
            font-size: 18px;
            float: left;
            padding-top: 5px;
            margin-right: 10px;
        }
    }
    .products-list{
        display: block;
        float: right;
        font-size: 18px;
    }
    .bottom-content{
        display: block;
        width: 100%;
        height: calc(100% - 120px);
    }
    .shortcuts{
        display: block;
        box-sizing: border-box;
        float: left;
        width: 60%;
        height: 100%;
        background: white;
        box-shadow: $boxshadow;
    }
    .box-title{
        display: block;
        position: relative;
        padding: $boxpadding;
        border-bottom: 1px solid gray;
        font-size: 26px;
    }
    .operational{
        display: block;
        box-sizing: border-box;
        width: 66%;
        float: left;
        padding: $boxpadding;
        span{
            font-size: 18px;
        }
    }
    .general{
        display: block;
        box-sizing: border-box;
        width: 33%;
        float: left;
        padding: $boxpadding;
        border-left: 1px solid gray;
        span{
            font-size: 18px;
        }
    }
    .buttons-operational{
        @extend %buttons;
        button{
            width: 45%;
            margin-right: 5%;
        }
    }
    .buttons-general{
        @extend %buttons;
        button{
            width: 100%;
        }
    }

    .alerts{
        display: block;
        box-sizing: border-box;
        float: left;
        width: 38%;
        margin-left: 2%;
        background: white;
        height: 100%;
        box-shadow: $boxshadow;
    }

    .alert-text{
        color: $lightblue;
    }
    .last-days{
        display: block;
        position: absolute;
        right: $boxpadding;
        top: $boxpadding;
        font-size: 12px;
    }
    .alert-content{
        display: block;
        box-sizing: border-box;
        width: 100%;
        float: left;
        padding: $boxpadding;
    }
    .alert-list{
        display: block;
        width: 100%;
        list-style: none;
        li{
            display: block;
            width: 100%;
            float: left;
            padding: 15px 0;
            font-size: 16px;
            border-bottom: 1px solid gray;
            &:first-child{
                padding-top: 0;
            }
            select{
                float: right;
                font-size: 16px;
            }
        }
    }
</style>

