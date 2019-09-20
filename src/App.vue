<template>
  <TemplateComponent></TemplateComponent>
</template>

<script>
import TemplateComponent from "./components/TemplateComponent.vue";

export default {
  name: "App",
  components: {
    TemplateComponent
  }
};
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
