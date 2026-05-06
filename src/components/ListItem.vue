<script setup>
    defineProps({
        nameItem: String,
        imageItem: String,
        status: Boolean,
        id: Number
    })

    const emit = defineEmits()
</script>

<template>
    <div class="card"
    :class="status ? 'card-bought' : 'card' "
    @click="emit('card-click', id)">
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

.card-bought {
    background-color: #393a39;
    width: 120px;
    padding: 3px;
    display: flex;
    flex-direction: column;
    align-items: center;
    border-radius: 5%;
    gap: 20px;
    cursor: pointer;
}

.card-bought img {
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