<template>
  <div class="title">
    <h2 class="main-title">{{mainTitle}}</h2>
    <p class="sub-title">{{subTitle}}</p>
  </div>
</template>

<script>
export default {
  props: {
    mainTitle: {
      type: String,
      default: ""
    },
    subTitle: {
      type: String,
      default: ""
    }
  }
};
</script>

<style lang="scss">
.title {
  @include title;
}
.main-title {
  @include main-title;
}
.sub-title {
  @include sub-title;
}
</style>