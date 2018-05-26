<template>
  <div id="app">
    <LandPageHeader/>
    <LandPageContent/>
    <LandPageFooter/>
  </div>
</template>

<script>
import LandPageContent from './components/LandPageContent'
import LandPageHeader from './components/LandPageHeader'
import LandPageFooter from './components/LandPageFooter'

export default {
  name: 'App',
  components: {
    LandPageHeader,
    LandPageContent,
    LandPageFooter
  }
}
</script>

<style src="./styles/main.scss" lang="scss"></style>
