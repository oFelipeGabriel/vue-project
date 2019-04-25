<template>
<div>
   <label>Multiplicacao: </label>{{mult}}<br>
   <label>Divisão: </label>{{dif}}<br>
   <label>Subtração: </label>{{sub}}<br>
</div>
</template>

<script>
export default {
    name: 'resultado',
    props: ['dados'],
    data: function(){
        return{
            e1: 0,
            e2: 0,
            mult: 0,
            dif: 0,
            sub: 0
        }
    },
    methods:{
        envia(){
            var dados = O
        }
    },
    watch:{
        dados: function(){
            this.e1 = this.dados.a;
            this.e2 = this.dados.b;
            this.mult = this.e1*this.e2;
            this.dif = this.e1/this.e2;
            this.sub = this.e1-this.e2;
        }
    }
}
</script>

<style>

</style>

