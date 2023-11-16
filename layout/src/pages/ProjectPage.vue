<template>
  <div>
    <HeaderComponent />
    <ProjectPageBaner />
    <ProjectPageContent />
    <FooterComponent />
  </div>
</template>

<script>
import HeaderComponent from '@/components/HeaderComponent.vue'
import FooterComponent from '../components/FooterComponent.vue'
import ProjectPageBaner from '../components/pagesComponents/ProjectPage/ProjectPageBaner.vue'
import ProjectPageContent from '../components/pagesComponents/ProjectPage/ProjectPageContent.vue'

export default {
  name: 'ProjectPage',
  data () {
    return {}
  },
  mounted () {
  },
  methods: {},
  components: {
    HeaderComponent,
    FooterComponent,
    ProjectPageBaner,
    ProjectPageContent
  }
}
</script>

<style lang="scss" scoped>
</style>
