<template>
  <div class="project__items">
    <div class="project__item" v-for="project in projects" :key="project.id">
      <img class="project__item-img" :src="require('@/assets/images/project_item/' + project.image)" alt="">
      <div class="project__item-wrap">
        <div class="project__item-wrap-text">
          <h2 class="project__item-title">{{ project.title }}</h2>
          <p class="project__item-text">{{ project.text }}</p>
        </div>
        <router-link to="/project-details">
          <svg xmlns="http://www.w3.org/2000/svg" width="70" height="70" viewBox="0 0 70 70" fill="none">
            <circle cx="35" cy="35" r="35" fill="#F4F0EC" />
            <path d="M32 44L40 35L32 26" stroke="#292F36" stroke-width="2" stroke-linecap="round"
              stroke-linejoin="round" />
          </svg>
        </router-link>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'ProjectPageProjects',
  props: ['projects'],

  data () {
    return {

    }
  },

  methods: {

  }
}
</script>

<style lang="scss" scoped>
@import "@/scss/vars";

.project__items {
  margin-top: 61px;
  margin-bottom: 61px;
  column-count: 2;
}

.project__item {
  padding-bottom: 27px;
  display: inline-block;

  &-wrap {
    display: flex;
    justify-content: space-between;
    align-items: center;
    flex-wrap: nowrap;
    flex-direction: row;
  }
}
</style>
