<template>
  <div class="project__categories">
    <div class="project__categories-wrap">
      <div :class="{ active: categories.activCategories }" class="project__categories-button"
        v-for="categories in categoriesList" :key="categories.id" @click="isActive(categories)">{{
          categories.nameCategories }}</div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'ProjectPageCategories',

  data () {
    return {
      categoriesList: [
        {
          id: 1,
          nameCategories: 'Bathroom',
          activCategories: false
        },
        {
          id: 2,
          nameCategories: 'Bed Room',
          activCategories: true
        },
        {
          id: 3,
          nameCategories: 'Kitchan',
          activCategories: false
        },
        {
          id: 4,
          nameCategories: 'Living Area',
          activCategories: false
        }
      ]
    }
  },

  methods: {
    isActive (data) {
      this.categoriesList.forEach(element => {
        element.activCategories = false
      })
      this.categoriesList[data.id - 1].activCategories = true
      this.$emit('activCategories', data)
      return this.categoriesList[data.id - 1].activCategories
    }
  }

}
</script>

<style lang="scss" scoped>
@import "@/scss/vars";

.project__categories {
  margin-top: 200px;
  display: flex;
  flex-direction: column;
  align-items: center;

  &-wrap {
    border-radius: 18px;
    width: 880px;
    border: 1px solid #CDA274;
    display: flex;
    justify-content: space-evenly;
    align-items: center;
    gap: 63px;
  }

  &-button {
    cursor: pointer;
    padding: 26px 66px;
    margin-left: -66px;
    margin-right: -66px;

    color: #292F36;
    text-align: center;
    font-family: $familyText;
    font-size: 18px;
    font-style: normal;
    font-weight: $font-600;
    line-height: 125%;
    letter-spacing: 0.36px;

    &:hover {
      color: #FFF;
      border-radius: 18px;
      background: #CDA274;
    }
  }

  .active {
    color: #FFF;
    border-radius: 18px;
    background: #CDA274;
  }
}
</style>
