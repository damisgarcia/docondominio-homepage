<template>
  <div>
    <header class="b-navigation">
      <div class="container">
        <nav class="navbar navbar-expand-lg navbar-light">
          <a class="navbar-brand flex align-items-center" href="#">
            <img src="@/assets/logo.png" width="98" alt="docondominio">
          </a>

          <b-btn v-b-toggle.collapse1 class="navbar-toggler">
            <span class="navbar-toggler-icon"></span>
          </b-btn>

          <b-collapse id="collapse1" class="navbar-collapse">
            <span class="mr-auto"></span>
            <b-nav class="navbar-nav justify-content-end">
              <b-nav-item active>Home</b-nav-item>
              <b-nav-item>Sobre</b-nav-item>
              <b-nav-item>Services</b-nav-item>
              <b-nav-item>Contact</b-nav-item>
            </b-nav>
          </b-collapse>
        </nav>
      </div>
    </header>
    <div class="landpage-header" v-bind:style="{ 'background-image':'url( '+ bg + ')' }">
      <div class="title">A maneira mais simples de gerênciar <br> o seu condomínio</div>
    </div>
  </div>
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
