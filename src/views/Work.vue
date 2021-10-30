<template>
  <div id="Work" style="height: 100%">
    <Navigation id="nav" />
    <v-main>
      <v-carousel
        height="100%"
        hide-delimiters
        cycle
        interval="2500"
        id="car"
        show-arrows-on-hover
        hide-delimiter-background
      >
        <v-carousel-item
          style="height: 100%"
          v-for="(item, i) in items"
          :key="i"
          :src="item.src"
        >
          <v-row class="fill-height title" align="center" justify="center">
            <div id="bDiv">
              <pre>{{ item.title }}<span v-if="item.title == 'WORKING'"> HARD</span><span v-if="item.title == 'CREAT'">       IVITY</span></pre>
            </div>
          </v-row>
        </v-carousel-item>
      </v-carousel>
    </v-main>
    <v-footer
      id="footer"
      class="pa-3"
      color="rgba(0,0,0,0.925)"
      height="37%"
      dark
      fixed
    >
      <v-spacer></v-spacer>
      <div class="caption">
        omar fostok &nbsp; &copy; {{ new Date().getFullYear() }}
      </div>
      <v-spacer></v-spacer>
    </v-footer>
  </div>
</template>
<script>
import Navigation from "../components/Navigation.vue";

export default {
  name: "Work",
  data() {
    return {
      items: [
        {
          src: require("../assets/images/rsz_rana-sawalha-w_-6pwgbyau-unsplash.jpg"),
          title: "WORKING",
        },
        {
          src: require("../assets/images/rsz_retro_closeup_camera_442946_1920x1080.jpg"),
          title: "PROFESSIONALITY",
        },
        {
          src: require("../assets/images/249675756_900854940549218_4005676627775797835_n.jpg"),
          title: "CREAT",
        },
      ],
    };
  },
  components: {
    Navigation,
  },
};
</script>
<style scoped>
#car {
  position: fixed;
  top: 0;
}
#bDiv {
  color: white;
  font-size: 8vw;
  text-shadow: 5px 10px 10px black;
  font-weight: bold;
}
#nav {
  position: fixed;
  width: 100%;
  top: 0;
  z-index: 10;
}
</style>