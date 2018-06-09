<template>
  <div>
    <header class="b-navigation">
      <div class="container">
        <nav class="navbar navbar-expand-lg navbar-dark">
          <a class="navbar-brand flex align-items-center" href="#">
            <img src="@/assets/white.svg" width="86" alt="docondominio">
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
      <div class="container">
        <div class="row">
          <div class="col-4 col-xs-12 device-col">
            <img class="img-fluid device" :src="device" />
          </div>
          <div class="col">
            <div class="title">Comunicação Simples e Eficiente</div>
            <div class="subtitle"><b>DoCondomínio</b> é uma plataforma de comunicação com um serviço <b>transparente, inteligente</b> e <b>intuitivo</b> para restabelecer a administração do seu condomínio de forma <b>eficaz</b> e <b>proativa</b>. Experimente!</div>
          </div>
        </div>
      </div>      
    </div>
  </div>
</template>
<script>
import bg from '@/assets/bg.png'
import device from '@/assets/device.png'

export default {
  name: 'LandPageHeader',
  data: () => {
    return {
      bg,
      device
    }
  }
}
</script>
