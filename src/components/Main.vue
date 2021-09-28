<template>
    <div class="container">
        <div class="film">
            <h3>FILM</h3>
            <ul class="cards">
                <Element v-for="card in cardMovie" :key="card.id" :item="card"/>
            </ul>
        </div>
        <div class="serieTv">
            <h3>SERIE TV</h3>
            <ul class="cards">
                <Element v-for="card in cardTv" :key="card.id" :item="card"/>
            </ul>
    </div>
</div>

</template>

<script>
import Element from './Element.vue'
export default {
  name: 'Main',
  components: {
      Element
    }, 
  props: ['cardMovie', 'cardTv']

}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
    .container {
        width: 100%;
        height: calc(100vh - 100px);
        background-color: gray;
    }
</style>
