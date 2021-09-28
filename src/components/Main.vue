<template>
    <div class="container">
        <ul class="card">
            <li v-for="(card, index) in cardMovie" :key="index">{{ card.title }} / {{ card.original_language }}</li>
        </ul>
    </div>
</template>

<script>
export default {
  name: 'Main',
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
