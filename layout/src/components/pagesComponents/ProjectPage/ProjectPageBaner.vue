<template>
  <section class="banner center">
    <div class="banner__intro">
      <h1 class="banner__intro-title">Our Project</h1>
      <p class="banner__intro-text">Home / Project</p>
    </div>
  </section>
</template>

<script>
export default {
  name: 'ProjectPageBaner',

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
@import "@/scss/vars";

.banner {
  background-image: url("@/assets/images/ProjectBaner.jpg");
  height: 356px;
  display: flex;
  justify-content: center;
  align-items: flex-end;

  &__intro {
    text-align: center;
    background: #fff;
    padding: 41px 78px;
    border-top-left-radius: 37px;
    border-top-right-radius: 37px;

    &-title {
      color: #292f36;
      font-family: $familyTitle;
      font-size: 50px;
      font-style: normal;
      font-weight: $font-400;
      line-height: 125%;
    }

    &-text {
      color: #4d5053;
      font-family: $familyText;
      font-size: 22px;
      font-style: normal;
      font-weight: $font-400;
      line-height: 150%;
      letter-spacing: 0.22px;
    }
  }
}
</style>
