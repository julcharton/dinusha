<template>
  <div class="wrapper">
    <sidebar />
    <div class="main">
      <blog-post v-bind="post" />
    </div>
  </div>
</template>

<script>
import sidebar from "@/components/sidebar";
import blogPost from "../components/blogpost";
import { mapState } from "vuex";

export default {
  components: {
    blogPost,
    sidebar
  },

  data() {
    return {
      id: this.$route.params.post
    };
  },
  computed: {
    ...mapState(["posts"]),
    post() {
      return this.posts.find(el => el.id === this.id);
    }
  }
};
</script>

<style scoped>
.main {
  margin-left: 17rem;
  padding: 0 0 0 6rem;
}
</style>