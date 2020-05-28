<template>
  <div class="home">
    <v-card class="mx-auto pa-5" elevation="20" max-width="500">
      <v-col>
        <h1 class="text-center ma-5">体温計どっかいった</h1>
        <p class="text-center">から適当に生成するサイト</p>

        <v-row justify="center">
          <v-switch
            align="center"
            class="text-center"
            v-model="is36Only"
            :label="`36度で固定する：${this.is36Only ? 'はい' : 'いいえ'}`"
          ></v-switch>
        </v-row>

        <p class="text-center ma-5" style="font-size:50px">{{temperature}}度</p>

        <v-btn
          class="text-center ma-2"
          block
          width="auto"
          color="primary"
          v-on:click="randomTemp()"
        >生成</v-btn>
      </v-col>
    </v-card>
  </div>
</template>

<script>
export default {
  name: "Home",
  components: {},
  data: () => ({
    temperature: "36.5",
    is36Only: true,
    isDarkMode: false
  }),
  methods: {
    randomTemp() {
      // ランダムで体温作る
      let min = 35;
      if (this.is36Only) {
        // 36度で固定する場合はtrue
        min = 36;
      }
      const max = 37;
      // 35~36の範囲で
      const temp = Math.floor(Math.random() * (max - min)) + min;
      const syousuuten = Math.ceil(Math.random() * 9);
      this.temperature = `${temp}.${syousuuten}`;
    }
  }
};
</script>
