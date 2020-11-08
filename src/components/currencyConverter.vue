<template>
    <div id="converter">
        <h1>Converta Real para Qualquer Moeda</h1>
        <label for="valueOnLocalCurrency" class="currencyInput">Valor em Reais:</label>
        <br>
        <input type="number" class="numberWithoutArrows" id="valueOnLocalCurrency" v-model="valueOnLocalCurrency">
        <br>
        <label for="valueOnExternCurrency" class="currencyInput">Valor em Dólares: </label>
        <br>
        <input type="number" class="numberWithoutArrows" id="valueOnExternCurrencyr" v-bind:value=dolar>
        <footer>
            <p>Site feito por <a href="github.com/stackovercrow">Gabriel dos Reis</a></p>
        </footer>
    </div>
</template>

<script>
export default{
    data(){
        return{
            valueOnLocalCurrency: "",
        }
    },

    computed:{
        dolar(){
            return this.valueOnLocalCurrency * 5;
        }
    }
}
</script>

<style>
    body{
        background-color: rgb(146, 228, 253);
        font-family: sans-serif;
        color: black;
    }

    h1{
        font-size: 18pt;
    }

    #converter{
        display: block;
        position: relative;
        text-align: center;
        font-family: sans-serif;
        background-color: rgb(97, 172, 233);
        width: 500px;
        height: 190px;
        position: absolute;
        border: black;
        border-style: dashed;
        top: 50%;
        left: 50%;
        transform: translate(-50%, -50%);
    }

    #converter .numberWithoutArrows{
        /* Chrome, Safari, Edge, Opera */
        -webkit-appearance: none;
        margin: 0;

        /* Firefox */
        -moz-appearance: textfield;
    }

    footer{
        margin-top: 0px;
        text-align: center;
    }

    a{
        text-decoration: none;
        color: black    ;
    }

</style>
