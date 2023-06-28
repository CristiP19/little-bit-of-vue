<template>
  <div className="app">
    <post-form @create="createPost"/>
    <post-list :posts="posts"/>
  </div>
</template>

<script>
import PostForm from "@/components/PostForm";
import PostList from "@/components/PostList";

export default {
  components: {
    PostForm,
    PostList,
  },
  data() {
    return {
      posts: [
        {id: 1, title: "Javascript 1", body: "Description 1"},
        {id: 2, title: "Javascript 2", body: "Description 2"},
        {id: 3, title: "Javascript 3", body: "Description 3"},
        {id: 4, title: "Javascript 4", body: "Description 4"},
      ],
    };
  },
  methods: {
    createPost(post) {
      this.posts.push(post);
    },
  },
};
</script>

<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

form {
  display: flex;
  flex-direction: column;
}

.app {
  padding: 20px;
}
</style>
