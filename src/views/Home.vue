<template>
  <div class="home" style="height: 100%">
    <!-- <img alt="Vue logo" src="../assets/logo.png"> -->
    <!-- <HelloWorld msg="Welcome to Your Vue.js App"/> -->
    <Navigation id="nav" />
    <v-main>
      <v-img
        src="@/assets/images/rsz_altumcode-dmut0x3f59q-unsplash.jpg"
        max-width="100%"
        max-height="100%"
        id="image"
      >
        <div class="test1 font-weight-bold">I'M OMAR FOSTOK</div>

        <div class="test2 font-weight-light font-italic">I am Freelancer,</div>
        <div class="test3 font-weight-light font-italic">
          Front-end Developer
        </div>
        <div class="line"></div>
      </v-img>
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

// @ is an alias to /src
// import HelloWorld from '@/components/HelloWorld.vue'

export default {
  name: "Home",
  components: {
    Navigation,
  },
};
</script>
<style scoped>
#footer {
  height: 100%;
}
#nav {
  position: fixed;
  width: 100%;
  top: 0;
  z-index: 10;
}
#image {
  margin-top: -70px;
  border-top: 64px solid black;
  position: fixed;
  top: 70px;
  height: 100%;
}

.test1 {
  text-shadow: 10px 10px 15px black;
  color: white;
  font-size: 5vw;
  border-radius: 5px;
  margin-left: 0px;
  position: fixed;
  top: 15vw;
  left: -1600px;
  animation-name: example;
  animation-duration: 6s;
  animation-iteration-count: infinite;
  width: 10000px;
  padding: 0px 25px;
}
@keyframes example {
  0% {
    left: -1600px;
  }

  40% {
    left: 3vw;
  }
  70% {
    left: 3vw;
  }
  80% {
    left: -1600px;
  }
  100% {
    left: -1600px;
  }
}

.test2 {
  color: white;
  font-size: 4.5vw;
  border-radius: 20px;
  text-shadow: 10px 10px 15px black;
  margin-left: 0px;
  position: fixed;
  left: -1600px;
  animation-name: example2;
  animation-duration: 6s;
  animation-iteration-count: infinite;
  width: 10000px;
  padding: 0px 25px;
}
.test3 {
  color: white;
  font-size: 4.5vw;
  border-radius: 5px;
  margin-left: 0px;
  text-shadow: 10px 10px 15px black;
  position: fixed;
  left: -1600px;
  animation-name: example3;
  animation-duration: 6s;
  animation-iteration-count: infinite;
  width: 10000px;
  padding: 0px 25px;
}
.line {
  width: 33vw;
  height: 0.25vw;
  border-radius: 50px;
  position: fixed;
  background-color: rgb(0, 119, 255);
  left: -1600px;
  top: 35vw;
  animation-name: example4;
  animation-iteration-count: infinite;
  animation-duration: 6s;
}
@keyframes example4 {
  0% {
    left: -1600px;
  }
  40% {
    left: -1600px;
  }
  48% {
    left: 5vw;
  }
  82% {
    left: 5vw;
  }
  95% {
    left: -1600px;
  }
  100% {
    left: -1600px;
  }
}
.test2 {
  top: 23vw;
}
.test3 {
  top: 28vw;
}
@keyframes example2 {
  0% {
    left: -1600px;
  }
  45% {
    left: 3vw;
  }
  75% {
    left: 3vw;
  }
  90% {
    left: -1600px;
  }
  100% {
    left: -1600px;
  }
}
@keyframes example3 {
  0% {
    left: -1600px;
  }
  50% {
    left: 3vw;
  }
  80% {
    left: 3vw;
  }
  95% {
    left: -1600px;
  }

  100% {
    left: -1600px;
  }
}
@media only screen and (max-width: 960px) {
  .line {
    height: 0.3vw;
  }
  @keyframes example4 {
    46% {
      left: -1600px;
    }
    55% {
      left: 6vw;
    }
    82% {
      left: 6vw;
    }
  }
}
@media only screen and (max-width: 520px) {
  .test1 {
    font-size: 8vw;
    top: 37vw;
  }
  .test2 {
    font-size: 7vw;
    top: 47vw;
  }
  .test3 {
    font-size: 7vw;
    top: 54vw;
  }
  @keyframes example4 {
    46% {
      left: -1600px;
    }
    55% {
      left: 9vw;
    }
    82% {
      left: 9vw;
    }
  }

  .line {
    width: 50vw;
    height: 0.3vw;
    border-radius: 20px;
    top: 63vw;
  }
}
</style>