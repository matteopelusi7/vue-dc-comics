<template>
  <header>

    <div class="container">

      <figure class="logo">
        <img src="../assets/img/dc-logo.png" alt="">
      </figure>
      
      <nav>
        <ul class="list-nav">
          <li v-for="(link, i) in links" :key="i">
            <a :class="( i == true ) ? 'active' : '' " :href="link.href">{{ link.text }}</a>
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
          href: '#',
          active: true
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
  min-height: 120px;

  .logo {
    width: 80px;
  }

  nav {
    min-height: 120px;
    display: flex;
  }

  .list-nav {
    display: flex;
    align-items: center;
    gap: 15px;
    flex-wrap: wrap;
    font-weight: 700;
    text-transform: uppercase;

      li {
        position: relative;
        min-height: 120px;
      }

      a {
        min-height: 120px;
        display: flex;
        align-items: center;
        font-size: 15px;
      }

      .active:after {
        content: '';
        display: block;
        height: 5px;
        background-color: dodgerblue;
        position: absolute;
        bottom: 0;
        width: 100%;
      }

      .active {
        color: dodgerblue;
      }

  }

}

</style>
