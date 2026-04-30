<script setup>
    import InviteImage from '../assets/InviteImage.png'
    import LogoImage from '../assets/LogoImage.jpg'
</script>


<template>
    <div class="container">
        <div class="invite">
            <img :src="InviteImage"/>
        </div>
        <div class="whatsapp-button">
            <h3>Botão do grupo</h3>
        </div>
        <div class="photo-carousel">
            <h3>Carrossel de imagens</h3>
        </div>
        <div class="logo">
            <img :src="LogoImage"/>
        </div>
    </div>
</template>

<style scoped></style>
