<template>
  <header class="header center">
    <div class="header__logo">
      <img src="../assets/images/Logo.jpg" alt="logo">
      <p class="logo__text">Interno</p>
    </div>
    <div class="header__menu">
      <router-link class="header__link" to="/">Home</router-link>
      <router-link class="header__link" to="/Project">Project</router-link>
      <router-link class="header__link" to="/Blog">Blog</router-link>
    </div>
  </header>
</template>

<script>
export default {
  name: 'HeaderComponent',

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
@import "../scss/vars";

.header {
  margin-top: 53px;
  margin-bottom: 57px;
  font-family: $familyTitle;
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: space-between;

  &__logo {
    display: flex;
    flex-wrap: nowrap;
    flex-direction: row;
    align-items: center;
    gap: 10px;
  }

  &__logo img {
    width: 34px;
    height: 34px;
  }

  &__logo p {
    font-size: 40px;
    font-style: normal;
    font-weight: $font-400;
    line-height: 125%;
    color: #292f36;
  }

  &__menu {
    text-align: center;
    font-family: $familyText;
    font-size: 20px;
    font-style: normal;
    font-weight: $font-400;
    line-height: 125%;
    display: flex;
    gap: 48px;
  }

  &__link {
    color: #292f36;
  }
}
</style>
