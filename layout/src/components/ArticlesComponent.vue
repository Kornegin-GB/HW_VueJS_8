<template>
  <article>
    <div class="blog__items">
      <div v-for="article in articlesPage" class="blog__item" :key="article.id">
        <div class="blog__item-image">
          <img :src="require('../assets/images/' + article.image)" :alt="article.image">
          <p class="blog__img-text">{{ article.imgText }}</p>
        </div>
        <h2 class="blog__item-title">{{ article.itemTitle }}</h2>
        <div class="blog__wrap-text">
          <p class="blog__item-text">{{ article.itemData }}</p>
          <router-link to="/blog-details">
            <svg xmlns="http://www.w3.org/2000/svg" width="53" height="53" viewBox="0 0 53 53" fill="none">
              <circle cx="26.5" cy="26.267" r="26" fill="#F4F0EC" />
              <path d="M24.271 32.9525L30.2139 26.2668L24.271 19.5811" stroke="#292F36" stroke-width="2"
                stroke-linecap="round" stroke-linejoin="round" />
            </svg>
          </router-link>
        </div>
      </div>
    </div>
    <div v-show="showBlok" class="count__page">
      <div class="count__page-wrap">
        <router-link class="count__page-number" v-for="page in totalPages" :key="`p${page}`" :to="`/blog/${page}`">
          <p class="count__page-number-text">{{ page }}</p>
        </router-link>
        <!-- <a href="#">
          <svg class="count__page-svg" xmlns="http://www.w3.org/2000/svg" width="53" height="52" viewBox="0 0 53 52"
            fill="none">
            <circle cx="26.5" cy="26" r="25.5" stroke="#CDA274" />
            <path d="M23.5571 32L29.5 25.3143L23.5571 18.6286" stroke="#292F36" stroke-width="2" stroke-linecap="round"
              stroke-linejoin="round" />
          </svg>
        </a> -->
      </div>
    </div>
  </article>
</template>

<script>
export default {
  name: 'ArticlesComponent',

  props: ['quantity', 'visible'],
  data () {
    return {
      articles: [
        {
          id: 1,
          image: 'blog_image_1.jpg',
          imgText: 'Kitchan Design',
          itemTitle: 'Let’s Get Solution For Building Construction Work',
          itemData: '26 December,2022'
        },
        {
          id: 2,
          image: 'blog_image_2.jpg',
          imgText: 'Living Design',
          itemTitle: 'Low Cost Latest Invented Interior Designing Ideas.',
          itemData: '22 December,2022'
        },
        {
          id: 3,
          image: 'blog_image_3.jpg',
          imgText: 'Interior Design',
          itemTitle: 'Best For Any Office & Business Interior Solution',
          itemData: '25 December,2022'
        },
        {
          id: 4,
          image: 'blog_image_3.jpg',
          imgText: 'Kitchan Design',
          itemTitle: 'Let’s Get Solution For Building Construction Work',
          itemData: '26 December,2022'
        },
        {
          id: 5,
          image: 'blog_image_2.jpg',
          imgText: 'Living Design',
          itemTitle: 'Low Cost Latest Invented Interior Designing Ideas.',
          itemData: '22 December,2022'
        },
        {
          id: 6,
          image: 'blog_image_1.jpg',
          imgText: 'Interior Design',
          itemTitle: 'Best For Any Office & Business Interior Solution',
          itemData: '25 December,2022'
        },
        {
          id: 7,
          image: 'blog_image_1.jpg',
          imgText: 'Kitchan Design',
          itemTitle: 'Let’s Get Solution For Building Construction Work',
          itemData: '26 December,2022'
        },
        {
          id: 8,
          image: 'blog_image_3.jpg',
          imgText: 'Living Design',
          itemTitle: 'Low Cost Latest Invented Interior Designing Ideas.',
          itemData: '22 December,2022'
        },
        {
          id: 9,
          image: 'blog_image_2.jpg',
          imgText: 'Interior Design',
          itemTitle: 'Best For Any Office & Business Interior Solution',
          itemData: '25 December,2022'
        },
        {
          id: 10,
          image: 'blog_image_3.jpg',
          imgText: 'Kitchan Design',
          itemTitle: 'Let’s Get Solution For Building Construction Work',
          itemData: '26 December,2022'
        },
        {
          id: 11,
          image: 'blog_image_1.jpg',
          imgText: 'Living Design',
          itemTitle: 'Low Cost Latest Invented Interior Designing Ideas.',
          itemData: '22 December,2022'
        },
        {
          id: 12,
          image: 'blog_image_2.jpg',
          imgText: 'Interior Design',
          itemTitle: 'Best For Any Office & Business Interior Solution',
          itemData: '25 December,2022'
        },
        {
          id: 13,
          image: 'blog_image_3.jpg',
          imgText: 'Kitchan Design',
          itemTitle: 'Let’s Get Solution For Building Construction Work',
          itemData: '26 December,2022'
        },
        {
          id: 14,
          image: 'blog_image_2.jpg',
          imgText: 'Living Design',
          itemTitle: 'Low Cost Latest Invented Interior Designing Ideas.',
          itemData: '22 December,2022'
        },
        {
          id: 15,
          image: 'blog_image_1.jpg',
          imgText: 'Interior Design',
          itemTitle: 'Best For Any Office & Business Interior Solution',
          itemData: '25 December,2022'
        },
        {
          id: 16,
          image: 'blog_image_1.jpg',
          imgText: 'Kitchan Design',
          itemTitle: 'Let’s Get Solution For Building Construction Work',
          itemData: '26 December,2022'
        }
      ]
    }
  },
  mounted () {

  },
  methods: {

  },
  computed: {
    showBlok () {
      return this.visible
    },
    totalPages () {
      return Math.ceil(this.articles.length / this.quantity)
    },
    currentPage () {
      return this.$route.params.page || 1
    },
    articlesPage () {
      const pageNumber = this.currentPage
      const startIndex = (pageNumber - 1) * this.quantity
      const endIndex = startIndex + this.quantity
      return this.articles.slice(startIndex, endIndex)
    }
  }
}
</script>

<style lang="scss" scoped>
@import "../scss/vars";

.blog {
  margin-top: 96px;
  margin-bottom: 96px;

  &__items {
    display: grid;
    grid-template-columns: repeat(3, 382px);
    gap: 27px;
  }

  &__item {
    border: 1px solid #e7e7e7;
    border-radius: 62px;
    padding: 21px;

    &-select {
      background: #f4f0ec;
    }
  }

  &__item-image {
    position: relative;

    & img {
      border-top-left-radius: 62px;
      border-top-right-radius: 62px;
      margin-bottom: 21px;
    }

    & p {
      position: absolute;
      top: 228px;
      left: 20px;
      border-radius: 8px 8px 8px 0px;
      background: #fff;
      padding: 4px 10px 8px 11px;
      color: #4d5053;
      font-family: $familyText;
      font-size: 16px;
      font-style: normal;
      font-weight: $font-400;
      line-height: 150%;
      letter-spacing: 0.16px;
      text-transform: capitalize;
    }
  }

  &__item-title {
    margin-bottom: 30px;
    color: #292f36;
    font-family: $familyTitle;
    font-size: 25px;
    font-style: normal;
    font-weight: $font-400;
    line-height: 125%;
    letter-spacing: 0.5px;
  }

  &__wrap-text {
    display: flex;
    flex-wrap: nowrap;
    flex-direction: row;
    justify-content: space-between;
    align-items: center;
  }

  &__item-text {
    color: #4d5053;
    font-family: $familyText;
    font-size: 16px;
    font-style: normal;
    font-weight: $font-400;
    line-height: 150%;
    letter-spacing: 0.16px;
    text-transform: capitalize;
  }
}

.count__page {
  margin-top: 51px;
  margin-bottom: 200px;
  display: flex;
  justify-content: center;

  &-wrap {
    display: flex;
    gap: 20px;
  }

  &-number {
    display: flex;
    justify-content: center;
    align-items: center;
    flex-wrap: nowrap;
    border: 1px #cda274 solid;
    width: 52px;
    height: 52px;
    border-radius: 52px;

    &-text {
      color: #292f36;
      font-family: $familyText;
      font-size: 16px;
      font-style: normal;
      font-weight: $font-500;
      line-height: 150%;
      text-transform: capitalize;
    }

    &:hover {
      background: #f4f0ec;
      border: none;
      width: 54px;
      height: 54px;
    }
  }

  &-svg:hover {
    fill: #f4f0ec;

    & circle {
      stroke: none;
    }
  }
}
</style>
