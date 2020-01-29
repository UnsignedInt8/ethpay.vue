<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png" />
    <!-- <HelloWorld /> -->
    <PayButton to="0x4ED9232873D1a0cac85d92497a5e9FA312Cfe30d" />
    <PayButton caption="Try with" to="0x4ED9232873D1a0cac85d92497a5e9FA312Cfe30d" title="Try with ETH Pay"/>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from "vue-property-decorator";
import HelloWorld from "./components/HelloWorld.vue";
import PayButton from "./components/PayButton.vue";

@Component({
  components: {
    HelloWorld,
    PayButton
  }
})
export default class App extends Vue {}
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
  display: flex;
  flex-direction: column;
  align-items: center;
}

#app > * {
  margin-bottom: 12px;
}
</style>
