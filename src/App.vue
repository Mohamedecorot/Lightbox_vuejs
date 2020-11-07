<template>
  <div id="app">
    <div v-if="title == 'nourriture'">
      <a :href="'http://lorempixel.com/800/600/food/' + n" v-lightbox v-for="n in 9" :key="n.id">
      <img :src="'http://lorempixel.com/150/150/food/' + n">
    </a>
    </div>    
    <div v-if="title == 'sport'">
      <a :href="'http://lorempixel.com/800/600/sports/' + n" v-lightbox v-for="n in 9" :key="n.id">
      <img :src="'http://lorempixel.com/150/150/sports/' + n">
    </a>
    </div>
    <button @click="title = 'sport'">SPORT</button>
    <button @click="title = 'nourriture'">NOURRITURE</button>
    <lightbox></lightbox>
  </div>
</template>

<script>
import Lightbox from './components/lightbox/Lightbox.vue'
export default {
  data () {
    return {
      title: 'sport'
    }
  },
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
