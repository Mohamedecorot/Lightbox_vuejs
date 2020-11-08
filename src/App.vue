<template>
  <div id="app">
    <div>
      <h1>LIGHTBOX</h1>
      <h3>Nourritures</h3>
      <a :href="'http://lorempixel.com/800/600/food/' + n" v-lightbox v-for="n in 9" :key="n.id">
        <img :src="'http://lorempixel.com/150/150/food/' + n">
      </a>
      <h3>Sports</h3>
      <a :href="'http://lorempixel.com/800/600/sports/' + n" v-lightbox="'sports'" v-for="n in 9" :key="n.id">
        <img :src="'http://lorempixel.com/150/150/sports/' + n">
      </a>
      <h3>nature</h3>
      <a :href="'http://lorempixel.com/800/600/nature/' + n" v-lightbox="'nature'" v-for="n in 9" :key="n.id">
        <img :src="'http://lorempixel.com/150/150/nature/' + n">
      </a>
      <h3>Technologie</h3>
      <a :href="'http://lorempixel.com/800/600/technics/' + n" v-lightbox="'technics'" v-for="n in 9" :key="n.id">
        <img :src="'http://lorempixel.com/150/150/technics/' + n">
      </a>
      <h3>Mode</h3>
      <a :href="'http://lorempixel.com/800/600/fashion/' + n" v-lightbox="'fashion'" v-for="n in 9" :key="n.id">
        <img :src="'http://lorempixel.com/150/150/fashion/' + n">
      </a>
      <h3>Gens</h3>
      <a :href="'http://lorempixel.com/800/600/people/' + n" v-lightbox="'people'" v-for="n in 9" :key="n.id">
        <img :src="'http://lorempixel.com/150/150/people/' + n">
      </a>
      <h3>Animaux</h3>
      <a :href="'http://lorempixel.com/800/600/animals/' + n" v-lightbox="'animals'" v-for="n in 9" :key="n.id">
        <img :src="'http://lorempixel.com/150/150/animals/' + n">
      </a>
    </div>
    <lightbox></lightbox>
  </div>
</template>

<script>
import Lightbox from './components/lightbox/Lightbox.vue'
export default {
  data () {
    return {
      title: 'food'
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
