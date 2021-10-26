<template>
  <v-app id="Image"> Hello World </v-app>
</template>
<script >
export default {
  name: "Image",
};
</script>
<style scoped>
#nav {
  position: sticky;
  top: 0;
  z-index: 10;
}
#image {
  margin-top: -70px;
  border-top: 70px solid black;
  position: fixed;
  top: 70px;
  height: 100%;
}
.test1 {
  font-family: "Anton", sans-serif;
  background-color: rgba(0, 0, 0, 0.5);
  color: white;
  font-size: 6vw;
  border-radius: 5px;
  margin-left: 0px;
  position: fixed;
  top: 25vw;
  left: -1600px;
  animation-name: example;
  animation-duration: 8s;
  animation-iteration-count: infinite;
  width: fit-content;
  padding: 0px 25px;
}
@keyframes example {
  0% {
    left: -1600px;
  }

  40% {
    left: 40px;
  }
  60% {
    left: 40px;
  }
  80% {
    left: -1600px;
  }
  100% {
    left: -1600px;
  }
}

.test2 {
  background-color: rgba(0, 0, 0, 0.5);
  color: white;
  font-size: 6vw;
  border-radius: 5px;
  margin-left: 0px;
  position: fixed;
  left: -1600px;
  animation-name: example2;
  animation-duration: 8s;
  animation-iteration-count: infinite;
  width: fit-content;
  padding: 0px 25px;
}
.test3 {
  background-color: rgba(0, 0, 0, 0.5);
  color: white;
  font-size: 6vw;
  border-radius: 5px;
  margin-left: 0px;
  position: fixed;
  left: -1600px;
  animation-name: example3;
  animation-duration: 8s;
  animation-iteration-count: infinite;
  width: fit-content;
  padding: 0px 25px;
}
.test2 {
  top: 15vw;
}
.test3 {
  top: 35vw;
}
@keyframes example2 {
  0% {
    left: -1600px;
  }
  45% {
    left: 40px;
  }
  70% {
    left: 40px;
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
  60% {
    left: 40px;
  }
  75% {
    left: 40px;
  }
  95% {
    left: -1600px;
  }

  100% {
    left: -1600px;
  }
}
</style>
