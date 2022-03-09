<template>
    
    <li class="card-item">
        <figure>
            <img :src="img" alt="">
        </figure>
        <p>{{ title }}</p>
    </li>

</template>

<script>
export default {
  name: 'CardMain',
  props: {
      img: String,
      title: String
  }
}
</script>

<style scoped lang="scss">

.card-item {

    flex-basis: calc( (100% / 6) - 15px);
    height: 220px;
    
    img {
      aspect-ratio: 1;
      object-fit: cover;
      object-position: top center;
    }

    p {
      text-transform: uppercase;
      padding: 15px 0;
    }

}

</style>
