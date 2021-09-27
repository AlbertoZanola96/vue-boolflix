<template>
  <header>
    <div class="title">
      <a href="/">BOOLFLIX</a>
    </div>
    <div class="search">  
      <input @keyup.enter="$emit('doResearch', inputText)" type="text" v-model="inputText" placeholder="Cerca su BOOLFLIX...">
      <button @click="$emit('doResearch', inputText)">Cerca</button>
    </div>
  </header>
</template>

<script>
export default {
  name: 'Header',
  data() {
    return {
      inputText:'',
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">

</style>
