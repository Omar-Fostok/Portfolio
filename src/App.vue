<template>
  <v-app>
    <router-view></router-view>
  </v-app>
</template>

<script>
// import HelloWorld from "./components/HelloWorld";

export default {
  name: "App",

  components: {
    // HelloWorld,
  },

  data: () => ({
    //
  }),
};
</script>
<style scoped >
/* 

Important note:
<p @click = "Go to About"> About </p>
methods: {
  GotoAbout() {
    this.$router.push('/about');
  }
}
*/
/* 
    <v-toolbar dark color="rgba(0,0,0,0.925)">
      <v-toolbar-title>Omar Fostok</v-toolbar-title>

      <v-spacer></v-spacer>
      <v-toolbar-items class="hidden-sm-and-down">
        <v-btn flat depressed color="transparent" class="class">Sign up</v-btn>

        <v-btn flat color="transparent" depressed>Log in</v-btn>
      </v-toolbar-items>
      <v-app-bar-nav-icon class="hidden-md-and-up"></v-app-bar-nav-icon>
    </v-toolbar>
*/
</style>
