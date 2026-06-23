<script setup>
import { ref, onMounted } from 'vue'

import LogoImage from '../assets/LogoImage.png'
import ListItem from '@/components/ListItem.vue'

const items = ref([])
const loading = ref(true)

async function loadItems() {
  loading.value = true

  const response = await fetch('https://bridal-shower-backend-0s12.onrender.com/items')

  const data = await response.json()

  items.value = data

  loading.value = false
}

async function changeStatus(id) {
  const answer = confirm('Confirme a escolha do item.')

  if (!answer) {
    return
  }

  await fetch(`https://bridal-shower-backend-0s12.onrender.com/items/${id}`, {
    method: 'PATCH',
  })

  await loadItems()
}

onMounted(() => {
  loadItems()
})
</script>

<template>
  <div class="container">
    <div class="title">
      <h1>Lista de Presentes</h1>
    </div>

    <div v-if="loading" class="loading">Carregando lista de presentes...</div>
    <div v-if="loading" class="loading">(Caso demore atualize a página)</div>

    <div class="gift-list">
      <ListItem
        v-for="item in items"
        :key="item.id"
        :id="item.id"
        :name-item="item.name"
        :image-item="item.image"
        :status="item.comprado"
        @card-click="!item.comprado && changeStatus(item.id)"
      />
    </div>

    <div class="logo">
      <img :src="LogoImage" />
    </div>
  </div>
</template>

<style scoped>
.gift-list {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 40px;
}

.loading {
  text-align: center;
  font-size: 1.2rem;
  color: #53674d;
}
</style>
