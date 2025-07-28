<template>
  <v-app>
    <v-app-bar
      app
      color="primary"
      dark>
      
      <v-spacer></v-spacer>
      <v-btn text to="/" tag="router-link">英単語検索</v-btn>
      <v-btn text to="/result" tag="router-link">検索結果</v-btn>
    </v-app-bar>

    <v-main>
      <router-view/>
    </v-main>
  </v-app>
</template>

<script>

export default {
  name: 'App',

  data: () => ({
    //
  }),
};
</script>
