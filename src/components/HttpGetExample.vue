<script setup>
import axios from "axios";
import { ref } from "vue";

const items = ref([]);

axios.get("https://jsonplaceholder.typicode.com/posts").then((resposne) => {
  items.value = resposne.data;
});
</script>

<template>
  <h1>Http Get Example</h1>
  <ul>
    <li v-for="item in items" :key="item.id">{{ item.title }}</li>
  </ul>
</template>
