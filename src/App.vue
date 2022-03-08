<template>
  <div id="app">
    <HeaderContent />
    <MainContent />
    <FooterContent />
  </div>
</template>

<script>

import HeaderContent from './components/Header.vue'
import MainContent from './components/Main.vue'
import FooterContent from './components/Footer.vue'

export default {
  name: 'App',
  components: {
    HeaderContent,
    MainContent,
    FooterContent,
  }
}

</script>

<style lang="scss">

* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

img {
  max-width: 100%;
}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
}
  
ul {
  list-style: none;
}
  
a {
  text-decoration: none;
  color: currentColor;
}

.container {
  margin: 0 auto;
  max-width: 1024px;
}

</style>
