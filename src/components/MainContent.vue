<template>
  <div class="container-box-big main-content">
    <app-search-bar></app-search-bar>
    <div v-if="loading">Loading...</div>
    <app-article v-else v-for="tip in tips" :key="tip.id" :tip="tip"></app-article>
  </div>
</template>

<script>
import AppSearchBar from "./SearchBar";
import AppArticle from "./Article";
import axios from "axios";

export default {
  components: {
    AppSearchBar,
    AppArticle
  },
  data() {
    return {
      tips: [],
      loading: true
    };
  },
  mounted() {
    axios
      .get("https://raendom-backend.z52da5wt.xyz/cache/tips")
      .then(({ data }) =>
        data.forEach(entry => {
          if (this.tips.length < 20) this.tips.push(entry);
          else return;
        })
      )
      .catch(err => console.log(err))
      .finally(() => {
        this.loading = false;
        console.log(this.tips);
      });
  }
};
</script>

<style scoped>
</style>