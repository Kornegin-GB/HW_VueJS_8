<template>
  <div>
    <HeaderComponent />
    <ProjectDetailsBanner />
    <ProjectDetailsContent />
    <FooterComponent />
  </div>
</template>

<script>
import HeaderComponent from '../components/HeaderComponent.vue'
import FooterComponent from '../components/FooterComponent.vue'
import ProjectDetailsBanner from '../components/pagesComponents/ProjectDetailsPage/ProjectDetailsBanner.vue'
import ProjectDetailsContent from '../components/pagesComponents/ProjectDetailsPage/ProjectDetailsContent.vue'

export default {
  components: { HeaderComponent, FooterComponent, ProjectDetailsBanner, ProjectDetailsContent },
  name: 'ProjectDetails',

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
