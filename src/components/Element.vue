<template>
    <div>
        <ul>
          <li><span>Titolo:</span> {{ item.title ? item.title : item.name}}</li>
          <!-- <li><span>Lingua:</span> {{ item.original_language }}</li> -->
          <img :src="require(`../assets/bandiere/${item.original_language}.png`)" alt="">
          <li><span>Voto:</span> {{ item.vote_average }}</li>
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

    span {
      font-size: 25px;
      font-weight: 600;
    }
  }
</style>
