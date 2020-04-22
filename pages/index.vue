<template>
  <div class="wrapper">
    <sidebar />

    <div class="main">
      <blog-post v-for="post in posts" :key="post" v-bind="post" :id="post.id" />
    </div>
  </div>
</template>

<script>
import blogPost from "../components/blogpost";
import sidebar from "@/components/sidebar";

export default {
  components: {
    blogPost,
    sidebar
  },
  methods: {
    handleScroll() {
      this.scrolled = window.scrollY > 0;
      console.log(this.scrolled);
    }
  },
  beforeMount() {
    window.addEventListener("scroll", this.handleScroll);
  },
  beforeDestroy() {
    window.removeEventListener("scroll", this.handleScroll);
  },
  data() {
    return {
      scrolled: false,
      posts: [
        {
          title: "The pretend One",
          id: "thePretendOne",
          banner: "The-pretendpone-banner.jpg",
          type: "Feature Film",
          year: "2017",
          description:
            "A heartwarming tale about a young female farmer, whose imaginary friend of the last 20 years only realizes he is in love with her when she starts to fall for a real man. Unable to face losing her, he must fight to become real himself.",
          credentials: {
            Director: ["Tony Prescott"],
            Producers: ["Tony Prescott & Dinusha Ratnaweera"],
            "Executive Producers": ["Kristina Ceyton & Samantha Jennings"],
            Cast: [
              "Geraldine Hakewill, Michael Whalley, Benedict Wall & David Field"
            ],
            Website: ["www.thepretendonefilm.com"]
          }
        },
        {
          title: "The pretend One",
          banner: "The-pretendpone-banner.jpg",
          type: "Feature Film",
          year: "2017",
          description:
            "A heartwarming tale about a young female farmer, whose imaginary friend of the last 20 years only realizes he is in love with her when she starts to fall for a real man. Unable to face losing her, he must fight to become real himself.",
          credentials: {
            Director: ["Tony Prescott"],
            Producers: ["Tony Prescott & Dinusha Ratnaweera"],
            "Executive Producers": ["Kristina Ceyton & Samantha Jennings"],
            Cast: [
              "Geraldine Hakewill, Michael Whalley, Benedict Wall & David Field"
            ],
            Website: ["www.thepretendonefilm.com"]
          }
        }
      ]
    };
  }
};
</script>

<style>
.main {
  margin-left: 17rem;
  padding: 0 0 0 6rem;
}
</style>