<template>
  <div id="app">
    <a :href="'http://placeimg.com/800/600/' + n" v-lightbox v-for="n in 9" :key="n.id">
      <img :src="'http://placeimg.com/150/150/' + n">
    </a>
    <lightbox></lightbox>
  </div>
</template>

<script>
import Lightbox from './components/lightbox/Lightbox.vue'
export default {
  components: {
    Lightbox
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
