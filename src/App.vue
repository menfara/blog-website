<template>
  <div class="app">
    <post-form
        @create="createPost"
    />
    <post-list
        :posts="posts"
    />


  </div>
</template>

<script>
import PostForm from "@/components/PostForm";
import PostList from "@/components/PostList";

export default {
  components: {
    PostList, PostForm
  },
  data() {
    return {
      posts: [
        {id: 1, title: 'Title', body: 'Body'},
        {id: 2, title: 'Title 1', body: 'Body 1'},
        {id: 3, title: 'Title 2', body: 'Body 2'},
      ],
    }
  },
  methods: {
    createPost(post) {
      this.posts.push(post);
    },

  }
}
</script>

<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

.app {
  padding: 20px;
}
</style>
