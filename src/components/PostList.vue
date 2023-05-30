<template>
  <div class="post" v-for="post in posts" :key="post.id">
    <div><strong>Title:</strong> {{ post.title }}</div>
    <div><strong>Body:</strong> {{ post.body }}</div>
  </div>
</template>

<script>
export default {
  props: {
    posts: {
      type: Array,
      required: true,
    }
  }
}
</script>

<style scoped>
.post {
  border: 1px solid #cccccc;
  padding: 10px;
  margin-top: 20px;
  background-color: #f9f9f9;
}

</style>