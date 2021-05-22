<template>
  <div class="flex flex-col min-h-screen lg:max-h-screen p-8 text-white">
    <Header/>
      <div class="flex flex-col flex-1 justify-around sm:text-2xl">
        <p class="text-2xl pt-8 font-bold self-center">
          stud/o<span class="ml-4 text-blue-400">w/ngress</span><br>
          <span class="text-gray-500">---------------</span>
        </p>
        <About class="pb-24 sm:pb-0"/>
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
