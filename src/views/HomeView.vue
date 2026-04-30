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
            <a href="https://chat.whatsapp.com/Ji8ugBsbG2sJliP2qIaYVC">
                Entre no nosso grupo do Whatsapp
            </a>
        </div>
        <div class="photo-carousel">
            <div class="track-images">
                <img :src="InviteImage"/>
                <img :src="InviteImage"/>
                <img :src="InviteImage"/>
                <img :src="InviteImage"/>
                <img :src="InviteImage"/>
            </div>
        </div>
        <div class="logo">
            <img :src="LogoImage"/>
        </div>
    </div>
</template>

<style scoped></style>
