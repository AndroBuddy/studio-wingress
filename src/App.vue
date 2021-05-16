<template>
  <div class="flex flex-col h-screen p-8 text-white">
    <Header/>
      <div :class="{'justify-center': isActive, 'font-bold': isActive}" class="flex flex-1 items-center sm:text-2xl">
        <p @mouseover="mouseIn" v-if="studio" class="cursor-pointer text-2xl">stud/o<span class="ml-4 text-blue-400">w/ngress</span>.</p>
        <div v-if="wingress" @click="about" class="cursor-pointer">
          <img src="./assets/logo.svg"/>
        </div>
        <About v-if="aboutVisibility"/>
      </div>
    <Footer class="invisible sm:visible h-0 sm:h-auto"/>
    <RespFooter class="visible sm:invisible sm:h-0"/>
  </div>
</template>

<script>
import Header from './components/Header.vue'
import Footer from './components/Footer.vue'
import About from './components/About.vue'
import RespFooter from './components/RespFooter.vue'

export default {
  name: 'App',
  components: {
    Header,
    Footer,
    About,
    RespFooter
  },
  data() {
    return {
      wingress: false,
      studio: true,
      aboutVisibility: false,
      isActive: true
    }
  },
  methods: {
    mouseIn: function() {
      this.wingress = true
      this.studio = false
    },
    about: function() {
      this.aboutVisibility = true
      this.wingress = false
      this.isActive = false
    }
  }
}
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Space+Mono:ital,wght@0,400;0,700;1,400&display=swap');

#app {
  font-family: 'Space Mono', monospace;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  background: #1D1A1A;
}
</style>
