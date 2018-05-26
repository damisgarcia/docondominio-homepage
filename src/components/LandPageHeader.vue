<template>
  <header class="landpage-header" v-bind:style="{ 'background-image':'url( '+ bg + ')' }">
    <img class="logo" width="128px" src='@/assets/white.svg' />
    <div class="title">A maneira mais simples de gerênciar <br> o seu condomínio</div>
    <div class="devices">
      <img src='@/assets/devices.png' />
      <small>Disponível na Apple Store e Playstore.</small>
    </div>
  </header>
</template>
<script>
import bg from '@/assets/bg.png'

export default {
  name: 'LandPageHeader',
  data: () => {
    return {
      bg
    }
  }
}
</script>
