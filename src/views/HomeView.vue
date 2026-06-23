<script setup>
import InviteImage from '../assets/InviteImage.png'
import LogoImage from '../assets/LogoImage.png'
import AnoNovoImage from '../assets/ano-novo.JPG'
import AparecidaImage from '../assets/aparecida.jpg'
import IrmaJoseliImage from '../assets/irma-joseli.JPG'
import NatalImage from '../assets/natal.JPG'
import NoivadoImage from '../assets/noivado.JPG'
</script>

<template>
  <div class="container">
    <div class="invite">
      <img :src="InviteImage" />
    </div>
    <div class="whatsapp-button">
      <a href="https://chat.whatsapp.com/Ji8ugBsbG2sJliP2qIaYVC">
        Entre no nosso grupo do Whatsapp
      </a>
    </div>
    <div class="photo-carousel">
      <div class="track-images">
        <img :src="AnoNovoImage" />
        <img :src="AparecidaImage" />
        <img :src="IrmaJoseliImage" />
        <img :src="NatalImage" />
        <img :src="NoivadoImage" />
        <img :src="AnoNovoImage" />
        <img :src="AparecidaImage" />
        <img :src="IrmaJoseliImage" />
        <img :src="NatalImage" />
        <img :src="NoivadoImage" />
      </div>
    </div>
    <div class="logo">
      <img :src="LogoImage" />
    </div>
  </div>
</template>

<style scoped></style>
