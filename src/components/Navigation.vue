<template>
  <div id="Navigation">
    <v-toolbar dark color="rgba(0,0,0,0.925)">
      <v-toolbar-title class="font-weight-bold font-italic" id="logo"
        >OMAR<span style="color: #1976d2">FOSTOK</span>
      </v-toolbar-title>

      <v-spacer></v-spacer>
      <v-spacer></v-spacer>
      <v-spacer></v-spacer>
      <v-spacer></v-spacer>
      <v-toolbar-items class="hidden-sm-and-down" id="mar">
        <v-btn
          exact-active-class="aa"
          text
          depressed
          v-ripple="false"
          id="btn1"
          class="btn"
          to="/"
          >HOME
          <div class="hello"></div>
          <div class="hello2"></div>
        </v-btn>
        <v-btn
          exact-active-class="aa"
          text
          depressed
          v-ripple="false"
          id="btn2"
          class="btn"
          to="/about"
          >ABOUT
          <div class="hello"></div>
          <div class="hello2"></div
        ></v-btn>
        <v-btn
          exact-active-class="aa"
          text
          depressed
          v-ripple="false"
          id="btn3"
          class="btn"
          to="/services"
          >SERVICES
          <div class="hello"></div>
          <div class="hello2"></div>
        </v-btn>
        <v-btn
          exact-active-class="aa"
          text
          depressed
          id="btn4"
          v-ripple="false"
          class="btn"
          to="/work"
          >WORK
          <div class="hello"></div>
          <div class="hello2"></div>
        </v-btn>
        <v-btn
          exact-active-class="aa"
          text
          depressed
          id="btn6"
          v-ripple="false"
          class="btn"
          to="/contact"
          >CONTACT
          <div class="hello"></div>
          <div class="hello2"></div>
        </v-btn>
      </v-toolbar-items>
      <v-row justify="center">
        <v-dialog max-width="600px">
          <template v-slot:activator="{ on, attrs }">
            <v-app-bar-nav-icon
              class="hidden-md-and-up"
              id="iconA"
              v-bind="attrs"
              v-on="on"
            ></v-app-bar-nav-icon>
          </template>
          <v-card>
            <v-btn tile color="black white--text" width="100%" to="/">
              HOME</v-btn
            >
            <v-btn tile color="black white--text" width="100%" to="/about"
              >ABOUT</v-btn
            >
            <v-btn tile color="black white--text" width="100%" to="/services"
              >SERVICES</v-btn
            >
            <v-btn tile color="black white--text" width="100%" to="/work"
              >WORK</v-btn
            >
            <v-btn tile color="black white--text" width="100%" to="/contact"
              >CONTACT</v-btn
            >
          </v-card>
        </v-dialog>
      </v-row>
    </v-toolbar>
  </div>
</template>
<script>
export default {
  name: "Navigation",
};
</script>
<style scoped>
.aa .hello2 {
  position: absolute;
  bottom: -6px;
  left: 0;
  width: 80%;
  height: 2px;
  background-color: white;
}

#logo {
  padding-right: 10px;
}
#btn1::before,
#btn2::before,
#btn3::before,
#btn4::before,
#btn6::before {
  background-color: transparent;
}
@import url("https://fonts.googleapis.com/css2?family=Anton&family=Cairo:wght@200;300;400;600;700;900&display=swap");
#btn1.btn,
#btn2.btn,
#btn3.btn,
#btn4.btn,
#btn5.btn,
#btn6.btn {
  color: white;
  background-color: transparent;
  font-size: 14px;
  position: relative;
  opacity: 1;
  transition-delay: 0s;
  transition-property: all;
}

#btn1.btn .hello,
#btn2.btn .hello,
#btn3.btn .hello,
#btn4.btn .hello,
#btn5.btn .hello,
#btn6.btn .hello {
  position: absolute;
  bottom: -6px;
  left: 0;
  width: 0;
  height: 2px;
  background-color: white;
  transition-duration: 0.4s;
  transition-property: all;
}

#btn1:hover,
#btn2:hover,
#btn3:hover,
#btn4:hover,
#btn5:hover,
#btn6:hover {
  background-color: transparent;
}
#btn1.btn:hover .hello,
#btn2.btn:hover .hello,
#btn3.btn:hover .hello,
#btn4.btn:hover .hello,
#btn5.btn:hover .hello,
#btn6.btn:hover .hello {
  width: 80%;
}
</style>
