<template>
  <div class="box m-2" v-bind:key="posts.id" v-for="post in posts">
    <h3>{{ post.text }}</h3>
  </div>
</template>

<script>
export default {
  name: "Comments",
  props: {
    posts: Array | Object,
  },
};
</script>

<style></style>
