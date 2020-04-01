<template>
  <ul>
    <li v-for="item in items" :key="item.name">
      <a :href="item.url">{{ item.name }}</a>
    </li>
  </ul>
</template>

<script>
export default {
  name: "SearchResult",
  props: ["items"]
};
</script>