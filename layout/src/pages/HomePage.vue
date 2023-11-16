<template>
  <div>
    <HeaderComponent></HeaderComponent>
    <HomePageBaner></HomePageBaner>
    <HomePageProject></HomePageProject>
    <HomePageCounter></HomePageCounter>
    <HomePageArticles></HomePageArticles>
    <FooterComponent></FooterComponent>
  </div>
</template>

<script>
import HeaderComponent from '../components/HeaderComponent.vue'
import HomePageBaner from '../components/pagesComponents/HomePage/HomePageBaner.vue'
import HomePageProject from '../components/pagesComponents/HomePage/HomePageProject.vue'
import HomePageCounter from '../components/pagesComponents/HomePage/HomePageCounter.vue'
import HomePageArticles from '../components/pagesComponents/HomePage/HomePageArticles.vue'
import FooterComponent from '../components/FooterComponent.vue'

export default {
  name: 'HomePage',

  components: {
    HeaderComponent,
    HomePageBaner,
    HomePageProject,
    HomePageCounter,
    HomePageArticles,
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
