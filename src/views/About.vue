<template>
  <div class="dark">
    <v-card class="mx-auto pa-5 ma-8" elevation="10" max-width="500">
      <v-row justify="center">
        <v-col>
          <h3 class="text-center">なにこれ</h3>
          <p class="text-center">Vue.js+Vuetifyで作った。しょーもな</p>
          <v-btn block color="primary" href="https://github.com/takusan23/TaionkeiDokkaitta" target="_blank">
            <v-icon>mdi-git</v-icon>ソースコード
          </v-btn>
        </v-col>
      </v-row>
    </v-card>
  </div>
</template>
<script>
export default {
  name: "About",
  components: {}
};
</script>
