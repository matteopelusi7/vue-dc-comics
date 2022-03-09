<template>
  <main>

    <div class="container">
      <p>{{ text }}</p>
    </div>
    
  </main>
</template>

<script>
export default {
  name: 'MainContent',
  data() {
    return {
      text: '--> Content goes here <--'
    }
  }
}
</script>

<style scoped lang="scss">

main {
  background: black;
  color: white;
  padding: 40px 0;
  font-weight: 800;
}

</style>
