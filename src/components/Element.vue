<template>
  <div class="container">
    <div class="copertina">
      <img class="imgCop" v-if="item.poster_path" :src="`https://image.tmdb.org/t/p/w342${item.poster_path}`"  alt="">
      <img class="imgCop" v-else src="https://img.flaticon.com/icons/png/512/120/120614.png?size=1200x630f&pad=10,10,10,10&ext=png&bg=FFFFFFFF" alt="">
    </div>
    <div class="info">
      <ul>
        <li><span>Titolo:</span> {{ item.title ? item.title : item.name}}</li>
        <img class="imgBand" :src="require(`../assets/bandiere/${item.original_language}.png`)" alt="">
        <li><span>Voto:</span> {{ item.vote_average }}</li>
      </ul>
    </div>
  </div>
</template>

<script>

export default {
  name: 'Element',
  props: ['item']
}

</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
  .container {
    .copertina {
      
      .imgCop {
        width: 140px;
        height: 200px;
      }
    }
  

    .info {
      margin-bottom: 10px;

      .info > ul {
        list-style: none;
      }

      .imgBand {
        width: 30px;
        height: 20px;
      }

      span {
        font-size: 25px;
        font-weight: 600;
      }
    }
  }
</style>
