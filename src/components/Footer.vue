<template>
  <footer>
    <div class="container">
      <div class="footer-info">
        <ul>
          <li v-for="(card, i) in cards" :key="i">
            <figure class="wrapper-img">
              <img :src= "card.img" alt="">
            </figure>
            {{ card.text }}
          </li>
        </ul>
      </div>
    </div>
    <div class="container-2">
      <div class="footer-list">
        <div class="container">
          <div class="list-wrapper">
            <div>
              <ul>
                <li>De Comics</li>
                <li>item</li>
                <li>item</li>
                <li>item</li>
                <li>item</li>
                <li>item</li>
                <li>item</li>
              </ul>
              <ul>
                <li>Shop</li>
                <li>item</li>
              </ul>
            </div>
            <div>
              <ul>
                <li>Dc</li>
                <li>item</li>
                <li>item</li>
                <li>item</li>
                <li>item</li>
                <li>item</li>
                <li>item</li>
                <li>item</li>
                <li>item</li>
                <li>item</li>
                <li>item</li>
                <li>item</li>
              </ul>
            </div>
            <div>
              <ul>
                <li>Sites</li>
                <li>item</li>
                <li>item</li>
                <li>item</li>
                <li>item</li>
                <li>item</li>
                <li>item</li>
              </ul>
            </div>
          </div>
          <div>
            <figure class="logo-bg">
              <img src="../assets/img/dc-logo-bg.png" alt="">
            </figure>
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
              <li>
                <img src="../assets/img/footer-facebook.png" alt="">
              </li>
              <li>
                <img src="../assets/img/footer-twitter.png" alt="">
              </li>
              <li>
                <img src="../assets/img/footer-youtube.png" alt="">
              </li>
              <li>
                <img src="../assets/img/footer-pinterest.png" alt="">
              </li>
              <li>
                <img src="../assets/img/footer-periscope.png" alt="">
              </li>
            </ul>
          </div>
        </div>
      </div>
    </div>
  </footer>
</template>

<script>
export default {
  name: 'FooterContent',
  data() {
    return {
      cards: [
        {
          text: 'DigitalComics',
          img: '../assets/img/buy-comics-digital-comics.png',
        },
        {
          text: 'DC Merchandise',
          img: '../assets/img/buy-comics-merchandise.png',
        },
        {
          text: 'Subscription',
          img: '../assets/img/buy-comics-shop-locator.png',
        },
        {
          text: 'Comic Shop Locator',
          img: '../assets/img/buy-comics-subsciption.png',
        },
        {
          text: 'DC Power Visa',
          img: '../assets/img/buy-comics-power-visa.png',
        },
      ]
    }
  }
}
</script>

<style scoped lang="scss">

footer {
  background-color: dodgerblue;
}

.container {

  padding: 30px 0;

  .footer-info .wrapper-img {
    width: 50px;
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
    gap: 10px;
  }

}

.footer-list {

  background-image: url('../assets/img/footer-bg.jpg');
  background-size: cover;
  background-repeat: no-repeat;
  background-position: center;

  .container {
    display: flex;
    justify-content: space-between;
    align-items: center;
    height: 300px;
  }

  .list-wrapper {
    display: flex;
    gap: 10px;
  }

  ul li:first-child {
    color: white;
    text-transform: uppercase;
    font-size: 16px;
    font-weight: 600;
    padding-bottom: 20px;
  }

  ul {
    padding: 10px 15px;
    color: rgb(128, 128, 128);
  }

}

.footer-social {

  background-color: rgb(54, 54, 54);

  .container {
    display: flex;
    justify-content: space-between;
  }

  .list-social {
    display: flex;
    align-items: center;
    gap: 15px;
  }

  .list-social li:first-child {
    color: dodgerblue;
    text-transform: uppercase;
  }

  .button {
    padding: 15px;
    border: 1px solid dodgerblue;
    background-color: rgb(54, 54, 54);
    color: white;
    text-transform: uppercase;
  }

}

</style>
