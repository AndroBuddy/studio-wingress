<template>
  <div class="flex flex-col h-screen p-8 text-white">
    <Header/>
      <div class="flex flex-1 justify-center items-center text-2xl font-bold">
        <p class="cursor-pointer">stud/o<span class="ml-4 text-blue-400">w/ngress</span>.</p>
      </div>
    <Footer/>
  </div>
</template>

<script>
import Header from './components/Header.vue'
import Footer from './components/Footer.vue'

export default {
  name: 'App',
  components: {
    Header,
    Footer
  }
}
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Space+Mono:ital,wght@0,400;0,700;1,400&display=swap');

#app {
  font-family: 'Space Mono', monospace;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  background: #1D1A1A;
}
</style>
