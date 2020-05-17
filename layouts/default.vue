<template>
  <v-app class="grey lighten-4">
    <!-- 上部のナビゲーションバー -->
    <v-app-bar class="primary" dark app>
      <v-app-bar-nav-icon
        class="hidden-md-and-up"
        @click="drawer = !drawer"
      ></v-app-bar-nav-icon>
      <v-toolbar-title class="text-uppercase">
        <span class="font-weight-light">Nakashin</span>
        <span>Portfolio</span>
      </v-toolbar-title>
      <v-spacer></v-spacer>
      <v-toolbar-items class="hidden-sm-and-down">
        <v-btn
          v-for="nav_list in nav_lists"
          :key="nav_list.name"
          :to="nav_list.to"
          text
          >{{ nav_list.name }}</v-btn
        >
      </v-toolbar-items>
    </v-app-bar>
    <!-- 横から出てくるドロワーのコンテンツ -->
    <v-navigation-drawer
      mobile-break-point
      app
      v-model="drawer"
      clipped
      class="hidden-md-and-up"
    >
      <v-container>
        <v-list-item>
          <v-list-item-content>
            <v-list-item-title class="title grey--text text--darken-2">
              Nakashin Portfolio
            </v-list-item-title>
          </v-list-item-content>
        </v-list-item>
        <v-divider></v-divider>
        <v-list dence nav>
          <v-list-item
            v-for="nav_list in nav_lists"
            :key="nav_list.name"
            :to="nav_list.to"
          >
            <v-list-item-icon>
              <v-icon>{{ nav_list.icon }}</v-icon>
            </v-list-item-icon>
            <v-list-item-content>
              <v-list-item-title>{{ nav_list.name }}</v-list-item-title>
            </v-list-item-content>
          </v-list-item>
        </v-list>
      </v-container>
    </v-navigation-drawer>
    <v-content class="ma-5 main-content">
      <nuxt />
    </v-content>
    <v-footer>
      <v-layout justify-center>
        <span>&copy; 2020 Nakano Shinya All Rights Reserved.</span>
      </v-layout></v-footer
    >
  </v-app>
</template>

<script>
export default {
  data() {
    return {
      drawer: false,
      nav_lists: [
        { name: "Home", icon: "mdi-home", to: "/" },
        { name: "About", icon: "mdi-account", to: "/about" },
        { name: "Skills", icon: "mdi-cogs", to: "/skills" },
        { name: "Works", icon: "mdi-palette", to: "/works" },
        { name: "Contact", icon: "mdi-email", to: "/contact" }
      ]
    };
  }
};
</script>

<style lang="scss">
body {
  font-family: "Open Sans", "Noto Sans JP", sans-serif;
  margin: 0;
}
</style>
