<script setup>
    import { ref } from 'vue'

    import LogoImage from '../assets/LogoImage.png'
    import ListItem from '@/components/ListItem.vue';

    import JogoCopo from '../assets/items/JogoCopo.webp'
    import JogoPrato from '../assets/items/JogoPrato.webp'
    
    function changeStatus(id) {
        for (const item of items.value){
            if (item.id === id){
                item.comprado = true
            }
        }
    }
    
    const items = ref(
        [
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
                'comprado': false
            },
            {
                'id': 2,
                'name': "Jogo de Prato",
                'image': JogoPrato,
                'comprado': false
            },
            {
                'id': 3,
                'name': "Jogo de Copos",
                'image': JogoCopo,
                'comprado':false
            },
            {
                'id': 4,
                'name': "Jogo de Copos",
                'image': JogoCopo,
                'comprado':false
            },
            {
                'id': 5,
                'name': "Jogo de Prato",
                'image': JogoPrato,
                'comprado': false
            },
            {
                'id': 6,
                'name': "Jogo de Prato",
                'image': JogoPrato,
                'comprado': false
            },
            {
                'id': 7,
                'name': "Jogo de Copos",
                'image': JogoCopo,
                'comprado':false
            },
            {
                'id': 8,
                'name': "Jogo de Copos",
                'image': JogoCopo,
                'comprado':false
            },
            {
                'id': 9,
                'name': "Jogo de Prato",
                'image': JogoPrato,
                'comprado': false
            },
            {
                'id': 10,
                'name': "Jogo de Prato",
                'image': JogoPrato,
                'comprado': false
            },
            {
                'id': 11,
                'name': "Jogo de Copos",
                'image': JogoCopo,
                'comprado':false
            },
        ]
    )


</script>

<template>
    <div class="container">
        <div class="title">
            <h1>Lista de Presentes</h1>
        </div>
        <div class="gift-list">
            <ListItem @card-click="changeStatus"
            v-for="item in items"
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
