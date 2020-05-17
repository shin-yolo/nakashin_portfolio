<template>
  <div class="skills-page">
    <Title mainTitle="Skills" subTitle="使用言語" />
    <v-container class="wrapper">
      <v-layout row wrap>
        <v-flex xs12 sm6 md4 v-for="skill in skills" :key="skill.language">
          <v-card class="text-center ma-3" height="250" color="grey lighten-4">
            <v-responsive class="pt-4">
              <v-avatar :size="100">
                <img :src="skill.avatar" aspect-ratio="1" />
              </v-avatar>
            </v-responsive>
            <v-card-text>
              <div class="subheading">{{ skill.language }}</div>
              <div class="grey--text">{{ skill.text }}</div>
            </v-card-text>
          </v-card>
        </v-flex>
      </v-layout>
    </v-container>
  </div>
</template>

<script>
export default {
  data() {
    return {
      skills: [
        {
          language: "HTML",
          text: "力強いレイアウトを作成することができます！",
          avatar: "/HTML.jpg"
        },
        {
          language: "CSS",
          text:
            "どのスクリーンサイズにも機能的なレスポンシブ対応のサイトを作成することが可能です。",
          avatar: "/css3.png"
        },
        {
          language: "JavaScript",
          text: "HTML＆CSSをもとに動的なサイトを作成することが可能です。",
          avatar: "/js.png"
        },
        {
          language: "Vue.js",
          text: "このポートフォリオを作成するにあたって習得しました。",
          avatar: "/vue-logo.png"
        },
        {
          language: "Nuxt.js",
          text:
            "このポートフォリオを作成するにあたって習得しました。がんばりました！！",
          avatar: "/nuxt_icon.png"
        },
        {
          language: "English",
          text:
            "大学１年の頃イギリスへ留学した経験があるので、英語は得意です。",
          avatar: "/english.png"
        }
      ]
    };
  }
};
</script>

<style lang="scss" scoped>
.wrapper {
  width: 90%;
  margin: 0 auto;
  max-width: $contentMaxWidth;
}
</style>