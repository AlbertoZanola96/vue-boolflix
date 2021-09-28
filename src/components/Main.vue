<template>
    <div class="container">
        <ul class="cards">
            <Element v-for="card in cardMovie" :key="card.id" :item="card"/>
        </ul>
    </div>
</template>

<script>
import Element from './Element.vue'
export default {
  name: 'Main',
  components: {
      Element
    }, 
  props: ['cardMovie']

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
