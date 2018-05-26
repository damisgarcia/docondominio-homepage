<template>
  <header class="landpage-header" v-bind:style="{ 'background-image':'url( '+ bg + ')' }">
    <h3>A maneira mais simples de gerênciar o seu condomínio</h3>
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
