<template>
  <img alt="Vue logo" src="./assets/female.jpg" class="inspired" />
  <Inspire msg="Get inspired" />
</template>

<script>
import Inspire from "./components/Inspire.vue";

export default {
  name: "App",
  components: {
    Inspire,
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
.inspired {
  height: 120px;
  border-radius: 50%;
  box-shadow: 5px 5px 5px brown;
}
</style>
