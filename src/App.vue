<template>
  <div id="app">
    <div class="container">
      <div class="paper">
        <LandPageHeader/>
        <LandPageContent/>
      </div>
    </div>
  </div>
</template>

<script>
import LandPageContent from './components/LandPageContent'
import LandPageHeader from './components/LandPageHeader'

export default {
  name: 'App',
  components: {
    LandPageHeader,
    LandPageContent
  }
}
</script>

<style src="./styles/main.scss" lang="scss"></style>
