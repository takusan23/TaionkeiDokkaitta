<template>
  <div class="dark">
    <v-card class="mx-auto pa-1 ma-8" elevation="10" max-width="300">
        <v-row justify="center">
          <v-switch
            class="text-center"
            append-icon="mdi-weather-night"
            v-model="$vuetify.theme.dark"
            :label="`ダークモード：${$vuetify.theme.dark ? 'はい' : 'いいえ'}`"
          ></v-switch>
        </v-row>
    </v-card>
  </div>
</template>
<script>
export default {
  name: "DarkSwitch",
  components: {}
};
</script>