<template>
    <div class="componente">
        <h2>Alterar os Dados de Usuário</h2>
        <p>Edite as informações</p>
        <p>{{usuarioIdade}}</p>
        <button @click="mudarIdade">++</button>
    </div>
</template>

<script>
export default {
    props:{
        usuarioIdade: {
            type: Number,
            required: true
        }
    },
    methods: {
        mudarIdade() {
            var userage = this.usuarioIdade
            userage++
            this.$emit('idadeMudou', userage)
        }
    }
}
</script>

<style scoped>
    .componente {
        flex: 1;
        background-color: #98b99a;
        color: #fff;
    }
</style>
