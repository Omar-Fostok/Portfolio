<template>
  <div id="Navigation">
    <v-toolbar dark color="rgba(0,0,0,0.925)">
      <v-toolbar-title class="font-weight-bold font-italic" id="logo"
        >OMAR FOSTOK
      </v-toolbar-title>

      <v-spacer></v-spacer>
      <v-spacer></v-spacer>
      <v-spacer></v-spacer>
      <v-spacer></v-spacer>
      <v-toolbar-items class="hidden-sm-and-down" id="mar">
        <v-btn text depressed id="btn1" class="btn" to="/">HOME</v-btn>
        <v-btn text depressed id="btn2" class="btn" to="/about">ABOUT</v-btn>
        <v-btn text depressed id="btn3" class="btn" to="/services"
          >SERVICES</v-btn
        >
        <v-btn text depressed id="btn4" class="btn" to="/work">WORK</v-btn>
        <v-btn text depressed id="btn6" class="btn" to="/contact"
          >CONTACT</v-btn
        >
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
            <v-btn tile color="black white--text" width="100%" to="/"
              >HOME</v-btn
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
#logo {
  padding-right: 10px;
}

#btn1.btn,
#btn2.btn,
#btn3.btn,
#btn4.btn,
#btn5.btn,
#btn6.btn {
  color: white;
  background-color: transparent;
  position: relative;
  opacity: 1;
  transition-delay: 0s;
  transition-property: all;
}
#btn1.btn::after,
#btn2.btn::after,
#btn3.btn::after,
#btn4.btn::after,
#btn5.btn::after,
#btn6.btn::after {
  content: "";
  position: absolute;
  bottom: 0;
  left: 0;
  width: 0px;
  height: 2px;
  background-color: white;
  transition-duration: 0.35s;
  transition-property: all;
}

#btn1.btn:hover,
#btn2.btn:hover,
#btn3.btn:hover,
#btn4.btn:hover,
#btn5.btn:hover,
#btn6.btn:hover {
  background-color: black;
}
#btn1.btn:hover::after,
#btn2.btn:hover::after,
#btn3.btn:hover::after,
#btn4.btn:hover::after,
#btn5.btn:hover::after,
#btn6.btn:hover::after {
  width: 100%;
}
</style>
