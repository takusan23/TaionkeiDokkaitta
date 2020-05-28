<template>
  <v-app>
    <v-content>
      <v-container fluid fill-height>
        <v-col>
          <router-view />
          <DarkModeSwitch />
        </v-col>
      </v-container>
    </v-content>
    <v-bottom-navigation :value="activeBtn" grow color="blue" >
      <v-btn to="/">
        <span>体温ランダム生成</span>
        <v-icon>mdi-account-heart-outline</v-icon>
      </v-btn>
      <v-btn to="/about">
        <span>このアプリについて</span>
        <v-icon>mdi-git</v-icon>
      </v-btn>
    </v-bottom-navigation>
  </v-app>
</template>

<script lang="ts">
import Vue from "vue";
import HelloWorld from "./components/HelloWorld.vue";
import DarkModeSwitch from "./views/DarkModeSwitch.vue";

export default Vue.extend({
  name: "App",
  components: { DarkModeSwitch },
  data: () => ({
    activeBtn: 0
  })
});
</script>

<style>
/* フォント設定 */
@font-face {
  font-family: "Koruri";
  src: url("https://cdn.plusminus.io/font/webkoruri/20140628/WebKoruri.eot");
  src: url("https://cdn.plusminus.io/font/webkoruri/20140628/WebKoruri.eot?#iefix")
    format("embedded-opentype");
  src: url("https://cdn.plusminus.io/font/webkoruri/20140628/WebKoruri.woff")
      format("woff"),
    url("https://cdn.plusminus.io/font/webkoruri/20140628/WebKoruri.ttf")
      format("truetype");

  /*  for fuck'n chrome  */
  src: url(https://cdn.plusminus.io/font/webkoruri/20140628/WebKoruri.woff)
    format("woff");
}

#app {
  font-family: Koruri;
}
</style>

