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
  header {
    width: 100%;
    height: 100px;
    background-color: black;
    display: flex;
    align-items: center;
    justify-content: space-between;

    .title > a {
      color: red;
      font-size: 26px;
      text-decoration: none;
      margin-left: 50px;
    }

    .search {
      margin-right: 50px;
    }
  }
</style>
