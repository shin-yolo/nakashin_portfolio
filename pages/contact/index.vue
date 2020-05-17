<template>
  <div class="page-about">
    <Title mainTitle="Contact" subTitle="お問い合わせ" />

    <v-container>
      <v-layout row wrap>
        <v-flex v-for="item in items" :key="item.name">
          <v-card flat class="text-center">
            <v-responsive class="pb-4">
              {{ item.name }}
            </v-responsive>
            <v-btn depressed large :href="item.to" nuxt>
              <v-icon>{{ item.icon }}</v-icon>
            </v-btn>
          </v-card>
        </v-flex>
      </v-layout>
    </v-container>
    <div>
      <p>
        質問、お問い合わせなどございましたら、各SNSのダイレクトメッセージまたはメールでご連絡ください。
      </p>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      items: [
        {
          name: "Twitter",
          icon: " fa-twitter",
          to: "https://twitter.com/shin_yolo1006"
        },
        {
          name: "Email",
          icon: " fa-envelope",
          to: "mailto:shinya.nakano106@gmail.com"
        },
        {
          name: "Instagram",
          icon: " fa-instagram",
          to: "https://www.instagram.com/ns_kny106/?hl=ja"
        }
      ]
    };
  }
};
</script>

<style lang="scss" scoped>
p {
  text-align: center;
  margin-top: 30px;
}
</style>
