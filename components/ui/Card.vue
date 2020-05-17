<template>
  <article class="card">
    <div class="card__img">
      <img :src="require(`~/assets/img/${imageUrl}`)" alt />
    </div>
    <div class="card__textbox">
      <h3 class="card__title">{{ title }}</h3>
      <p class="card__text">{{ text }}</p>
      <v-btn @click="onClickLink" small>CHECK</v-btn>
    </div>
  </article>
</template>

<script>
export default {
  props: {
    imageUrl: {
      type: String,
      required: true
    },
    title: {
      type: String,
      required: true
    },
    text: {
      type: String,
      required: true
    },
    href: {
      type: String,
      default: true
    },
    newTab: {
      type: Boolean,
      default: false
    }
  },
  methods: {
    onClickLink() {
      if (this.newTab === true) {
        window.open(this.href, "_blank");
      } else {
        window.location.href = this.href;
      }
    }
  }
};
</script>

<style lang="scss" scoped>
.card {
  width: 288px;
  height: auto;
  box-shadow: 0 3px 6px #ccc;

  &__img > img {
    width: 100%;
    height: auto;
    background-size: cover;
    box-sizing: border-box;
  }
  &__textbox {
    width: 100%;
    height: auto;
    padding: 20px 18px;
    background: #ffffff;
    box-sizing: border-box;
  }
  &__title {
    font-size: 20px;
    font-weight: bold;
    line-height: 125%;
    margin-bottom: 5px;
  }
  &__text {
    font-size: 12px;
    line-height: 150%;
    margin-bottom: 5px;
  }
}
</style>