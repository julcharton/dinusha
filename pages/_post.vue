<template>
    <div class="main">
      <blog-post v-bind="post" />

  </div>
</template>

<script>
import sidebar from "@/components/sidebar";
import blogPost from "../components/blogpost";
import { mapState } from "vuex";

export default {
  components: {
    blogPost

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

<style>

.main{
  width: stretch;
  overflow: auto;

}
</style>