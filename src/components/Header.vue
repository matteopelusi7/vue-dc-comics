<template>
  <header>
    <div class="container">
      <figure class="logo">
        <img src="../assets/img/dc-logo.png" alt="">
      </figure>
      <nav>
        <ul class="list-nav">
          <li v-for="(link, i) in links" :key="i">
            <a :href="link.href">{{ link.text }}</a>
          </li>
        </ul>
      </nav>
    </div>
  </header>
</template>

<script>
export default {
  name: 'HeaderContent',
  data() {
    return {
      links: [
        {
          text: 'Characters',
          href: '#'
        },
        {
          text: 'Comics',
          href: '#'
        },
        {
          text: 'Movies',
          href: '#'
        },
        {
          text: 'Tv',
          href: '#'
        },
        {
          text: 'Games',
          href: '#'
        },
        {
          text: 'Collectibles',
          href: '#'
        },
        {
          text: 'Video',
          href: '#'
        },
        {
          text: 'Fans',
          href: '#'
        },
        {
          text: 'News',
          href: '#'
        },
        {
          text: 'Shop',
          href: '#'
        },
      ]
    }
  }
}
</script>

<style scoped lang="scss">

.container {

  display: flex;
  align-items: center;
  justify-content: space-between;
  flex-wrap: wrap;
  padding: 30px 10px;

  .logo {
    width: 80px;
  }

  .list-nav {
    display: flex;
    align-items: center;
    gap: 10px;
    flex-wrap: wrap;
    font-weight: 700;
    text-transform: uppercase;
  }

}

</style>
