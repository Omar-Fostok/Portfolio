<template>
  <div class="about">
    <Navigation id="nav" />
    <v-main id="cont">
      <v-container class="grey lighten-5" id="about">
        <v-row style="background-color: rgb(240, 240, 240)">
          <v-col cols="12" sm="12" md="8">
            <v-card
              class=""
              outlined
              tile
              style="background-color: rgb(240, 240, 240)"
            >
              <v-simple-table dark id="table">
                <template v-slot:default>
                  <tbody>
                    <tr v-for="item in desserts" :key="item.name">
                      <td>{{ item.name }}</td>
                      <td>{{ item.value }}</td>
                    </tr>
                  </tbody>
                </template>
              </v-simple-table>
            </v-card>
          </v-col>
          <v-col cols="12" sm="12" md="4">
            <v-card
              class="pa-2"
              outlined
              tile
              style="
                background-color: rgb(240, 240, 240);
                border: 1px solid rgb(200, 200, 200);
              "
            >
              <h2>ABOUT ME:</h2>
              <p>
                Curabitur non nulla sit amet nisl tempus convallis quis ac
                lectus. Curabitur arcu erat, accumsan id imperdiet et, porttitor
                at sem. Praesent sapien massa, convallis a pellentesque nec,
                egestas non nisi. Nulla porttitor accumsan tincidunt. Mauris
                blandit aliquet elit, eget tincidunt nibh pulvinar a. Vivamus
                suscipit tortor eget felis porttitor volutpat. Vestibulum ac
                diam sit amet quam vehicula elementum sed sit amet dui.
                porttitor at sem. Nulla porttitor accumsan tincidunt. Quisque
                velit nisi, pretium ut lacinia in, elementum id enim. Nulla
                porttitor accumsan tincidunt. Mauris blandit.
              </p>
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
        {
          name: "HTML",
          value: "85%",
        },
        {
          name: "CSS",
          value: "75%",
        },
        {
          name: "JavaScript",
          value: "50%",
        },
        {
          name: "VueJs",
          value: "50%",
        },
        {
          name: "Bootstrap",
          value: "50%",
        },
      ],
    };
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
#nav {
  position: sticky;
  top: 0;
  z-index: 10;
}
#about {
  outline: 0 0 0 10px;
  outline-style: solid;
  outline-color: rgb(0, 119, 255);
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
  font-size: larger;
  text-align: center;
}
h2 {
  width: fit-content;
  margin: auto;
  border-bottom: 2px solid rgb(0, 119, 255);
  margin-bottom: 50px;
}

#nav {
  position: sticky;
  top: 0;
  z-index: 10;
}
</style>
