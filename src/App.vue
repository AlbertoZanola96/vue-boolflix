<template>
  <div id="app">
    <Header @doResearch="ricerca"/>

    <Main :cardMovie="film" :cardTv="serie"/>
  </div>
</template>

<script>
import axios from 'axios';
import Header from './components/Header.vue';
import Main from './components/Main.vue';

export default {
  name: 'App',
  components: {
    Header,
    Main
  },
  data() {
    return {
      apiUrl: "https://api.themoviedb.org/3/search/",
      apiKey: 'f5b8768754bedd89a3401c68be8ae40d',
      film: [],
      serie: [],
    }
  },
  methods: {
    ottieniFilm(apiParams) {
      axios.get(this.apiUrl + "movie", apiParams).then((response) => {
        this.film = response.data.results;
      });
    },
      ottieniSerie(apiParams) {
        axios.get(this.apiUrl + "tv", apiParams).then((response) => {
          this.serie = response.data.results;
      });
    },
    ricerca(searchText) {
      const paramsObj = {
        params: {
          api_key: this.apiKey,
          query: searchText,
        },
      };
      this.ottieniFilm(paramsObj);
      this.ottieniSerie(paramsObj);
    },
  }
}
</script>

<style lang="scss">
  * {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
  }
</style>
