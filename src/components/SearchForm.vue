<template>
  <form>
    <input type="text" v-model="key">
  </form>
</template>

<script>
export default {
  name: "SearchForm",
  props: ["keyword"],
  data: function() {
    return {
      key: ""
    };
  }
};
</script>