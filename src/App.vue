<template>
  <div id="app">
    <form>
      <input type="text" v-model="keyword">
    </form>
    <SearchResult :items="filteredList"/>
  </div>
</template>

<script>
// import SearchForm from "./components/SearchForm";
import SearchResult from "./components/SearchResult";

export default {
  name: "App",
  data: function() {
    return {
      keyword: "",
      result: [
        { name: "Google", url: "https://google.com" },
        { name: "Microsoft", url: "https://microsoft.com" },
        { name: "Yahoo", url: "https://yahoo.com" },
        { name: "Facebook", url: "https://facebook.com" },
        { name: "Twitter", url: "https://twitter.com" },
        { name: "Instagram", url: "https://instagram.com" },
        { name: "Pinterest", url: "https://pinterest.com" }
      ]
    };
  },
  components: {
    // SearchForm,
    SearchResult
  },
  computed: {
    filteredList() {
      return this.result.filter(item => {
        return item.name.toLowerCase().includes(this.keyword.toLowerCase());
      });
    }
  }
};
</script>