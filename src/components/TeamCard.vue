<template>
    <div class= "card text-white bg-dark">
        <div class= "d-flex justify-content-center p-2">
            <img :src= "member.image" alt="Fotografía">
        <div>
        <div class= "card-body">
            <h3 class "card-title"> {{member.nombre}}</h3>
            <p.class="card-text">{{member.descripcion}}</p>
            <p.class="card-text"><span>Código:</span>{{member.codigo}}</p>
            <p.class="card-text"><span>Rol:</span>{{member.rol}}</p>
        <div>
    </div>
</template>

<script>
    export default {
        name: "TeamCard",
        props: ['member']
    }
</script>

<style scoped>

</style>
