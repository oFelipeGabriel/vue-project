<template>
<div>
    <h1>Olá mundo</h1>
    <label for="entrada1">A: </label>
    <input class="inputEntrada" type="number" id="entrada1" v-model="e1"><br>
    <label for="entrada2">B: </label>
    <input class="inputEntrada"  type="number" id="entrada2" v-model="e2"><br>
    <input id="btnCalc" type="button" value="Calcular" @click="envia">
    </div>
</template>

<script>
export default {
    name: 'entrada',
    data: function(){
        return{
            e1: 0,
            e2: 0,
        }
    },
    methods:{
        envia(){
            var dados = Object();
            dados.a = this.e1;
            dados.b = this.e2;
            this.$emit('envia', dados);
        }
    }
}
</script>

<style>
#btnCalc{
    margin: 10px 0;
    padding: 5px;
    border-radius: 5px;
}
.inputEntrada{
    margin: 5px 0;
    line-height: 15px;
    padding: 3px;
    border-radius: 5px;
    border: 1 px solid grey;
}
</style>

