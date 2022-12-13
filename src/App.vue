<template>
  <div id="app">
    <HeaderComponent/>
   
    <ContentComponent/>
    <FooterComponent/>
    <DetailsComponent></DetailsComponent>
  </div>
</template>

<script>
import FooterComponent from './components/FooterComponent.vue'
import HeaderComponent from './components/HeaderComponent.vue'
import ContentComponent from './components/ContentComponent.vue'
import DetailsComponent from './components/DetailsComponent.vue'
export default {
  name: 'App',
  components: {
    FooterComponent,
    HeaderComponent,
    ContentComponent,
    DetailsComponent
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
