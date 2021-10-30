<template>
  <div class="about">
    <Navigation id="nav" />
    <v-main id="cont">
      <v-container class="blue lighten-5" id="about">
        <v-row
          style="
            background-color: rgb(240, 240, 240);
            border: 2px solid #1976d2;
            border-radius: 5px;
          "
        >
          <v-col cols="12" sm="12" md="12" lg="8">
            <v-row>
              <v-col cols="12">
                <v-card class="" style="background-color: rgb(240, 240, 240)">
                  <v-simple-table height="100%" dark id="table">
                    <template v-slot:default>
                      <tbody>
                        <tr v-for="item in desserts" :key="item.name">
                          <td style="width: 50%">{{ item.name }}</td>
                          <td style="width: 50%">{{ item.value }}</td>
                        </tr>
                      </tbody>
                    </template>
                  </v-simple-table>
                </v-card>
              </v-col>
            </v-row>
            <v-row>
              <v-col>
                <div class="c">
                  <div class="html">85%</div>
                  <h4>HTML</h4>
                  <v-lazy transition="scroll-x-transition">
                    <v-progress-linear value="85%" rounded> </v-progress-linear>
                  </v-lazy>
                </div>

                <br />
                <div class="c">
                  <div class="css">75%</div>
                  <h4>CSS</h4>
                  <v-lazy transition="scroll-x-transition">
                    <v-progress-linear value="75%" rounded> </v-progress-linear>
                  </v-lazy>
                </div>
                <br />
                <div class="c">
                  <div class="java">50%</div>
                  <h4>JavaScript</h4>
                  <v-lazy transition="scroll-x-transition">
                    <v-progress-linear value="50%" rounded> </v-progress-linear>
                  </v-lazy>
                </div>
                <br />
                <div class="c">
                  <div class="boot">60%</div>
                  <h4>Bootstrap</h4>
                  <v-lazy transition="scroll-x-transition">
                    <v-progress-linear value="60%" rounded> </v-progress-linear>
                  </v-lazy>
                </div>
                <br />
                <div class="c">
                  <div class="vue">70%</div>
                  <h4>VueJs</h4>
                  <v-lazy transition="scroll-x-transition">
                    <v-progress-linear value="70%" rounded> </v-progress-linear>
                  </v-lazy>
                </div>
              </v-col>
            </v-row>
          </v-col>
          <v-col cols="12" sm="12" md="12" lg="4">
            <v-card
              class="pa-2"
              outlined
              style="
                background-color: rgb(240, 240, 240);
                border: 1px solid rgb(240, 240, 240);
              "
            >
              <v-lazy transition="scroll-x-transition">
                <h2>About me</h2>
              </v-lazy>
              <v-lazy transition="scroll-x-reverse-transition">
                <p>
                  Curabitur non nulla sit amet nisl tempus convallis quis ac
                  lectus. Curabitur arcu erat, accumsan id imperdiet et,
                  porttitor at sem. Praesent sapien massa, convallis a
                  pellentesque nec, egestas non nisi. Nulla porttitor accumsan
                  tincidunt. Mauris blandit aliquet elit, eget tincidunt nibh
                  pulvinar a. Vivamus suscipit tortor eget felis porttitor
                  volutpat. Vestibulum ac diam sit amet quam vehicula elementum
                  sed sit amet dui. porttitor at sem. Nulla porttitor accumsan
                  tincidunt. Quisque velit nisi, pretium ut lacinia in,
                  elementum id enim. Nulla porttitor accumsan tincidunt. Lorem
                  ipsum, dolor sit amet consectetur adipisicing elit. Temporibus
                  ab veniam maxime laudantium.
                </p>
              </v-lazy>
            </v-card>
          </v-col>
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
  name: "About",
  components: {
    Navigation,
  },
  data() {
    return {
      desserts: [
        {
          name: "First Name:",
          value: "Omar",
        },
        {
          name: "Last Name:",
          value: "Fostok",
        },
        {
          name: "Profile:",
          value: "Front-end Developer",
        },
        {
          name: "Email:",
          value: "omar6817167@gmail.com",
        },
        {
          name: "Country:",
          value: "Syria",
        },
        {
          name: "Phone:",
          value: "+963945281526",
        },
      ],
    };
  },
};
</script>
<style scoped>
.c {
  position: relative;
}
.html {
  position: absolute;
  left: 85%;
}
.css {
  position: absolute;
  left: 75%;
}
.java {
  position: absolute;
  left: 50%;
}
.boot {
  position: absolute;
  left: 60%;
}
.vue {
  position: absolute;
  left: 70%;
}
#table {
  background-color: #1976d2;
  color: white;
}
#cont {
  background-color: rgba(255, 255, 255, 0.05);
}
#footer {
  height: 100%;
  position: absolute;
  bottom: 0;
  width: 100%;
}
#nav {
  position: sticky;
  top: 0;
  z-index: 10;
}
#about {
  border-radius: 5px;
  box-shadow: 0px 0px 20px black;
  margin-top: 130px;
  margin-bottom: 153.5px;
}
.about {
  background-image: url("../assets/images/550656.jpg");
  background-size: cover;
  height: 100%;
}

p {
  font-family: "Cairo", sans-serif;
  font-size: larger;
}
h2 {
  width: fit-content;
  margin: auto;
  margin-bottom: 50px;
  position: relative;
}
h2:after {
  content: "";
  position: absolute;
  background-color: rgb(0, 119, 255);
  bottom: 0;
  left: 0;
  height: 2px;
  width: 70%;
}

tr:hover {
  background-color: rgb(86, 145, 209) !important;
}

td {
  padding: 13.7px !important;
  text-align: left;
}
#nav {
  position: sticky;
  top: 0;
  z-index: 10;
}
</style>
