<template>
  <section class="blog center">
    <h2 class="blog__title-left">Articles & News</h2>
    <ArticlesComponent :quantity="6" :visible="true"></ArticlesComponent>
  </section>
</template>

<script>
import ArticlesComponent from './../../ArticlesComponent.vue'

export default {
  name: 'BlogPageBlogs',

  components: {
    ArticlesComponent
  }
}
</script>

<style lang="scss" scoped>
@import "@/scss/vars";

.blog__title-left {
  text-align: left;
  margin-top: 150px;
  margin-bottom: 30px;
  color: #292f36;
  font-family: $familyTitle;
  font-size: 50px;
  font-style: normal;
  font-weight: $font-400;
  line-height: 125%;
  letter-spacing: 1px;
}
</style>
