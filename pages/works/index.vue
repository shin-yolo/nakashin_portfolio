<template>
  <div class="page-about">
    <!-- <TheHeader /> -->
    <Title main-title="Works" sub-title="作品" />

    <div class="card-wrapper">
      <Card
        image-url="work.png"
        title="架空のジム"
        text="自分が初めて作ったポートフォリオです"
        href="http://nakashin-yolo.com/"
        :new-tab="true"
      />
      <Card
        image-url="work.png"
        title="架空のジム"
        text="自分が初めて作ったポートフォリオです"
        href="http://nakashin-yolo.com/"
        :new-tab="true"
      />
      <Card
        image-url="work.png"
        title="架空のジム"
        text="自分が初めて作ったポートフォリオです"
        href="http://nakashin-yolo.com/"
        :new-tab="true"
      />
      <Card
        image-url="portfolio.png"
        title="自己紹介用ポートフォリオ"
        text="２つ目のポートフォリオです"
        href="http://happy-edison-a9075c.netlify.com"
        :new-tab="true"
      />
      <Card
        image-url="portfolio.png"
        title="自己紹介用ポートフォリオ"
        text="２つ目のポートフォリオです"
        href="http://happy-edison-a9075c.netlify.com"
        :new-tab="true"
      />
      <Card
        image-url="portfolio.png"
        title="自己紹介用ポートフォリオ"
        text="２つ目のポートフォリオです"
        href="http://happy-edison-a9075c.netlify.com"
        :new-tab="true"
      />
    </div>
  </div>
</template>
<script></script>
<style scoped lang="scss">
.page-about {
  width: 90%;
  margin: 0 auto;
  max-width: $contentMaxWidth;
}
.card-wrapper {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  grid-gap: 2em;
  justify-items: center;
}

@media screen and (max-width: 1000px) {
  .card-wrapper {
    grid-template-columns: repeat(2, 1fr);
    justify-items: center;
  }
}

@media screen and (max-width: 600px) {
  .card-wrapper {
    grid-template-columns: repeat(1, 1fr);
    justify-items: center;
  }
}
</style>
