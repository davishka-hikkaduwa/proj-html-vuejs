<template>
  <div id="app">
    <HeaderComponent/>
    <MainComponent/>
    <FooterComponent/>
  </div>
</template>

<script>
import HeaderComponent from '@/components/HeaderComponent.vue';
import MainComponent from '@/components/MainComponent.vue';
import FooterComponent from '@/components/FooterComponent.vue';

export default {
  name: 'App',
  components: {
    HeaderComponent,
    MainComponent,
    FooterComponent
}
}
</script>

<style lang="scss">
body{
    margin: 0;
    padding: 0;   
}
#app {
  @import '@/assets/styles/style.scss';
  @import '@/assets/styles/utilities.scss';
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  margin: 0;
  padding: 0;
  // width: 100vw;
  
}
</style>
