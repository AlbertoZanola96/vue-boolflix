<template>
    <div>
        <ul>
          <li><h4>Titolo:</h4> {{ item.title }}</li>
          <!-- <li><h4>Lingua:</h4> {{ item.original_language }}</li> -->
          <img :src="require(`../assets/bandiere/${item.original_language}.png`)" alt="">
          <li><h4>Voto:</h4> {{ item.vote_average }}</li>
        </ul>
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
  div {
    // width: 100px;
    // height: 200px;
    // background-color: pink;
    margin-bottom: 10px;

    ul {
      list-style: none;
    }

    img {
      width: 30px;
      height: 20px;
    }
  }
</style>
