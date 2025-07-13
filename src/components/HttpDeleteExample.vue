<script setup>
import axios from "axios";

const handleDelete = () => {
  axios
    .delete(`https://jsonplaceholder.typicode.com/posts/1`)
    .then((response) => {
      console.log("Post created:", response.data);
    })
    .catch((error) => {
      console.log("Error creating post:", error);
    });
};
</script>

<template>
  <h1>Http Delete Example</h1>
  <button @click="handleDelete">Delete Post</button>
</template>
