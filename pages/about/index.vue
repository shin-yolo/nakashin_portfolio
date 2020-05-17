<template>
  <div class="page-about">
    <Title mainTitle="About" subTitle="自己紹介" />
    <v-layout class="card-container" row wrap justify-space-around>
      <v-flex xs12 md5>
        <v-card v-for="about in abouts" :key="about.name" class="mb-8" min-height="300">
          <v-card-title class="headline text-xs-center">Me</v-card-title>

          <v-container class="nested">
            <div class="img">
              <v-avatar size="150" class="justify-center">
                <img src="/about.jpg" />
              </v-avatar>
            </div>
            <div class="card-text">
              <v-card-text>名前：{{ about.name }}</v-card-text>
              <v-card-text>年齢：{{ about.age }}</v-card-text>
              <v-card-text>現在：{{ about.now }}</v-card-text>
              <v-card-text>趣味：{{ about.hobby }}</v-card-text>
            </div>
          </v-container>
        </v-card>
      </v-flex>
      <v-flex xs12 md5>
        <v-card min-height="300">
          <v-card-title class="headline">Profile</v-card-title>
          <v-container>
            <v-card-text pa-5>
              都内の大学に通う大学３年中野慎也と申します。
              プログラミングは留学をきっかけに知りました。プログラミングを学習していくうちにITの世界に魅了され、現在はWebエンジニアになるためプログラミング学習に日々励んでおります。
            </v-card-text>
          </v-container>
        </v-card>
      </v-flex>
    </v-layout>
  </div>
</template>

<script>
export default {
  data() {
    return {
      abouts: [
        {
          name: "中野慎也",
          age: 20,
          now: "大学生",
          hobby: "筋トレ週7,プログラミング"
        }
      ]
    };
  }
};
</script>

<style lang="scss" scoped>
.card-container {
  width: 95%;
  margin: 0 auto;
  max-width: $contentMaxWidth;
}
.nested {
  display: grid;
  grid-template-columns: 1fr 2fr;
  grid-gap: 10px;
}

@media screen and (max-width: 400px) {
  .nested {
    grid-template-columns: 1fr;
  }
}
</style>
