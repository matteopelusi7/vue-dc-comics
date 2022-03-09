<template>
  <footer>

    <div class="container">
      
      <CategoriesMain />

    </div>

    <div class="container-2">

      <div class="footer-list">

        <div class="container">

          <div class="list-wrapper">

            <div>
              <ul>
                <li v-for="(item, i) in items1" :key="i">{{ item }}</li>
              </ul>
              <ul>
                <li v-for="(item, i) in items2" :key="i">{{ item }}</li>
              </ul>
            </div>
            <div>
              <ul>
                <li v-for="(item, i) in items3" :key="i">{{ item }}</li>
              </ul>
            </div>
            <div>
              <ul>
                <li v-for="(item, i) in items4" :key="i">{{ item }}</li>
              </ul>
            </div>
          </div>

        </div>

      </div>

      <div class="footer-social">
        <div class="container">
          <div>
            <button class="button">Sign-Up Now!</button>
          </div>
          <div>
            <ul class="list-social">
              <li>Follow Us</li>
              <li v-for="(item, i) in items5" :key="i">
                <img :src="item.img" alt="">
              </li>
            </ul>
          </div>
        </div>
      </div>
    </div>

  </footer>
</template>

<script>

import CategoriesMain from '../components/Categories.vue'

export default {

  components: {
    CategoriesMain
  },

  data() {
    return {
      items1:['Dc Comics', 'Characters', 'Comics','Movies', 'TV', 'Games', 'Videos', 'News'],
      items2:['Shop', 'Shop DC', 'Shop DC Collectibles'],
      items3:['DC', 'Terme Of Use', 'Privacy policy (New)', 'Ad Choises', 'Advertising', 'Jobs', 'Subscriptions', 'Talent Workshops', 'CPSC Certificates', 'Ratings', 'Shop Help', 'Contact Us'],
      items4:['DC', 'MAD MAgazine', 'DC Kids', 'DC Universe', 'DC Power Visa'],
      items5:[
        {
          img: require('../assets/img/footer-facebook.png')
        },
        {
          img: require('../assets/img/footer-twitter.png')
        },
        {
          img: require('../assets/img/footer-youtube.png')
        },
        {
          img: require('../assets/img/footer-pinterest.png')
        },
        {
          img: require('../assets/img/footer-periscope.png')
        },
      ]
    }
  },

  name: 'FooterContent',
  
}
</script>

<style scoped lang="scss">

footer {
  background-color: dodgerblue;
}

.container {

  padding: 30px 0;

}

.footer-list {

  background-image: url('../assets/img/footer-bg.jpg');
  background-size: cover;
  background-repeat: no-repeat;
  background-position: center;

  .container {
    background-image: url('../assets/img/dc-logo-bg.png');
    background-repeat: no-repeat;
    background-position: 90% 45%;
    background-size: auto;
    display: flex;
    justify-content: space-between;
    align-items: center;
  }

  .list-wrapper {
    display: flex;
    gap: 5px;

    li {
      line-height: 20px;
    }

  li {
    cursor: pointer;
  }

  }

  ul li:first-child {
    color: white;
    text-transform: uppercase;
    font-size: 16px;
    font-weight: 600;
    padding-bottom: 20px;
  }

  ul {
    padding: 10px 10px;
    color: rgb(128, 128, 128);
    font-size: 14px;
  }

}

.footer-social {

  background-color: rgb(54, 54, 54);

  .container {
    display: flex;
    justify-content: space-between;
    align-items: center;
    gap: 10px;
  }

  .list-social {
    display: flex;
    align-items: center;
    gap: 20px;
    cursor: pointer;
  }

  .list-social li:first-child {
    font-weight: 700;
    color: dodgerblue;
    text-transform: uppercase;
  }

  .button {
    padding: 15px;
    border: 2px solid dodgerblue;
    background-color: rgb(54, 54, 54);
    color: white;
    text-transform: uppercase;
    cursor: pointer;
    font-weight: 700;
  }

}

</style>
