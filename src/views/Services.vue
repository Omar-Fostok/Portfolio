<template>
  <div class="Services">
    <Navigation id="nav" />
    <v-main id="body">
      <v-container class="grey lighten-5" id="con">
        <h2 class="hidden-lg-and-up" style="margin-top: 10%">SERVICES</h2>
        <v-row id="rowy">
          <v-col cols="12" sm="6" md="6" lg="4" id="r">
            <v-card class="mx-auto my-12" max-width="374" id="card1">
              <v-img
                height="250"
                src="../assets/images/diego-ph-fIq0tET6llw-unsplash.jpg"
                id="timg1"
              ></v-img>

              <h3>Web Design</h3>

              <div class="pad">
                Lorem, ipsum dolor sit amet consectetur adipisicing elit.
                Laborum alias accusamus distinctio eos! Unde rerum quibusdam
                illum adipisci quasi repudiandae delectus, repellendus incidunt
                dolores dolorum assumenda doloremque, magnam itaque magni. Lorem
                ipsum dolor sit amet consectetur, adipisicing elit. Cupiditate
                dolore natus doloribus?
              </div>
            </v-card>
          </v-col>
          <v-col cols="12" sm="6" md="6" lg="4" id="s">
            <h2 class="hidden-md-and-down">SERVICES</h2>
            <v-card class="mx-auto my-12" max-width="374" id="card2">
              <v-img
                height="250"
                src="../assets/images/karl-pawlowicz-QUHuwyNgSA0-unsplash.jpg"
              ></v-img>

              <h3>Web Development</h3>

              <div class="pad">
                Lorem, ipsum dolor sit amet consectetur adipisicing elit.
                Laborum alias accusamus distinctio eos! Unde rerum quibusdam
                illum adipisci quasi repudiandae delectus, repellendus incidunt
                dolores dolorum assumenda doloremque, magnam itaque magni. Lorem
                ipsum dolor sit amet consectetur, adipisicing elit. Cupiditate
                dolore natus doloribus?
              </div>
            </v-card>
          </v-col>
          <v-col cols="12" sm="6" md="6" lg="4" id="t">
            <v-card class="mx-auto my-12" max-width="374" id="card3">
              <v-img
                height="250"
                src="../assets/images/istockphoto-1299482876-612x612.jpg"
              ></v-img>

              <h3>Responsive Design</h3>

              <div class="pad">
                Lorem, ipsum dolor sit amet consectetur adipisicing elit.
                Laborum alias accusamus distinctio eos! Unde rerum quibusdam
                illum adipisci quasi repudiandae delectus, repellendus incidunt
                dolores dolorum assumenda doloremque, magnam itaque magni. Lorem
                ipsum dolor sit amet consectetur, adipisicing elit. Cupiditate
                dolore natus doloribus?
              </div>
            </v-card>
          </v-col>
          <v-col class="hidden-lg-and-up hidden-sm-and-down"></v-col>
        </v-row>
      </v-container>
    </v-main>
    <v-footer
      id="footer"
      class="pa-3"
      color="rgba(0,0,0,0.925)"
      height="37%"
      dark
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
  name: "Services",
  components: {
    Navigation,
  },
};
</script>
<style scoped>
#footer {
  height: 100%;
  position: absolute;
  bottom: 0;
  width: 100%;
}
#con {
  background-color: transparent !important;
}
.Services {
  background-image: url("../assets/images/firmbee-com-GANqCr1BRTU-unsplash.jpg");
  background-size: cover;
  height: 100%;
}
#nav {
  position: sticky;
  top: 0;
  z-index: 10;
}

#r,
#s,
#t {
  text-align: center;
}
#r {
  margin-top: -70px;
}
h2 {
  color: white;
  background-color: rgba(0, 0, 0, 0.85);
  width: fit-content;
  padding: 0px 20px;
  margin: auto;
  margin-bottom: -20px;
  margin-top: -40px;
  border-radius: 10px;
  font-size: 40px;
  box-shadow: 0px 0px 10px black;
  text-align: center;
}
#t {
  margin-top: 70px;
}
h3 {
  padding: 10px;
  font-size: x-large;
}
#card1,
#card2,
#card3 {
  box-shadow: 1px 3px 7px rgba(0, 0, 0, 0.692);
  background-color: rgb(240, 240, 240);
}
#rowy {
  margin-top: 80px;
  margin-bottom: 22px;
  background-color: transparent;
}
.pad {
  padding: 20px;
}
#body {
  background-color: rgba(0, 0, 0, 0.5);
}
@media only screen and (max-width: 1264px) {
  #rowy {
    margin-top: 0;
    margin-bottom: 0;
  }
  #r {
    margin-top: 0;
  }
  #t {
    margin-top: 0;
  }
}
</style>