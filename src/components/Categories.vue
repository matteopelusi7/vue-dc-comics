<template>
  <div class="footer-info">

        <ul>
          <li v-for="(card, i) in cards" :key="i">
            <figure class="wrapper-img">
              <img :src="card.img" alt="">
            </figure>
            {{ card.text }}
          </li>
        </ul>

      </div>
</template>

<script>
export default {
  name: 'CategoriesFooter',
  data() {
    return {
      cards: [
        {
          text: 'DigitalComics',
          img: require('../assets/img/buy-comics-digital-comics.png'),
        },
        {
          text: 'DC Merchandise',
          img: require('../assets/img/buy-comics-merchandise.png'),
        },
        {
          text: 'Subscription',
          img: require('../assets/img/buy-comics-shop-locator.png'),
        },
        {
          text: 'Comic Shop Locator',
          img: require('../assets/img/buy-comics-subscriptions.png'),
        },
        {
          text: 'DC Power Visa',
          img: require('../assets/img/buy-dc-power-visa.svg'),
        },
      ]
    }
  }
}
</script>


<style scoped lang="scss">

  .footer-info .wrapper-img {
    width: 40px;
  }

  .footer-info ul {
    display: flex;
    gap: 20px;
    flex-wrap: wrap;
    color: white;
    text-transform: uppercase;
    font-size: 12px;
  }

  .footer-info ul li {
    display: flex;
    align-items: center;
    justify-content: center;
    gap: 10px;
    flex-grow: 1;
  }

</style>
