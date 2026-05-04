<script setup>
    import LogoImage from '../assets/LogoImage.png'
    import ListItem from '@/components/ListItem.vue';

    import JogoCopo from '../assets/items/JogoCopo.webp'
    import JogoPrato from '../assets/items/JogoPrato.webp'
    const items = [
        {
            'id': 0,
            'name': "Jogo de Copos",
            'image': JogoCopo,
            'comprado':false
        },
        {
            'id': 1,
            'name': "Jogo de Prato",
            'image': JogoPrato,
            'comprado': true
        },
        {
            'id': 2,
            'name': "Jogo de Prato",
            'image': JogoPrato,
            'comprado': true
        },
        {
            'id': 3,
            'name': "Jogo de Copos",
            'image': JogoCopo,
            'comprado':false
        },
        {
            'id': 0,
            'name': "Jogo de Copos",
            'image': JogoCopo,
            'comprado':false
        },
        {
            'id': 1,
            'name': "Jogo de Prato",
            'image': JogoPrato,
            'comprado': true
        },
        {
            'id': 2,
            'name': "Jogo de Prato",
            'image': JogoPrato,
            'comprado': true
        },
        {
            'id': 3,
            'name': "Jogo de Copos",
            'image': JogoCopo,
            'comprado':false
        },
        {
            'id': 0,
            'name': "Jogo de Copos",
            'image': JogoCopo,
            'comprado':false
        },
        {
            'id': 1,
            'name': "Jogo de Prato",
            'image': JogoPrato,
            'comprado': true
        },
        {
            'id': 2,
            'name': "Jogo de Prato",
            'image': JogoPrato,
            'comprado': true
        },
        {
            'id': 3,
            'name': "Jogo de Copos",
            'image': JogoCopo,
            'comprado':false
        },
    ]

</script>

<template>
    <div class="container">
        <div class="title">
            <h1>Lista de Presentes</h1>
        </div>
        <div class="gift-list">
            <ListItem v-for="item in items"
            :id="item.id"
            :name-item="item.name"
            :image-item="item.image"
            :status="item.comprado"
            :key="item.id"/>
        </div>
        <div class="logo">
            <img :src="LogoImage"/>
        </div>
    </div>
</template>


<style scoped>
.gift-list {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 40px;
}
</style>
