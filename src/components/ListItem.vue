<script setup>
    defineProps({
        nameItem: String,
        imageItem: String
    })
</script>

<template>
    <div class="card"
    @click="console.log('Funcionando')">
        <img :src="imageItem">
        <p>{{nameItem}}</p>
    </div>
</template>

<style scoped>


.card {
    background-color: #53674d;
    width: 120px;
    padding: 3px;
    display: flex;
    flex-direction: column;
    align-items: center;
    border-radius: 5%;
    gap: 20px;
    cursor: pointer;
}

.card img {
    width: 100px;
    height: 100px;
    border-radius: 5%;
    margin-top: 10px;
    object-fit: cover;
}

.card p {
    color: #fff;
    font-size: 16px;
    margin-top: -10px;
    margin-bottom: 10px;
    text-align: center;
}
</style>