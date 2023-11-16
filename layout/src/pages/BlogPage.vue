<template>
  <div>
    <HeaderComponent></HeaderComponent>
    <BlogPageBaner></BlogPageBaner>
    <BlogPageLastPost></BlogPageLastPost>
    <BlogPageBlogs></BlogPageBlogs>
    <FooterComponent></FooterComponent>
  </div>
</template>

<script>
import HeaderComponent from '../components/HeaderComponent.vue'
import BlogPageBaner from '../components/pagesComponents/BlogPage/BlogPageBaner.vue'
import BlogPageLastPost from '../components/pagesComponents/BlogPage/BlogPageLastPost.vue'
import BlogPageBlogs from '../components/pagesComponents/BlogPage/BlogPageBlogs.vue'
import FooterComponent from '../components/FooterComponent.vue'
export default {
  name: 'BlogPage',

  components: {
    HeaderComponent,
    BlogPageBaner,
    BlogPageLastPost,
    BlogPageBlogs,
    FooterComponent
  },

  data () {
    return {

    }
  },

  mounted () {

  },

  methods: {

  }
}
</script>

<style lang="scss" scoped>

</style>
