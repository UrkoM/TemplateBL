<template>
  <!-- Código HTML:
  Dentro de la etiqueta "Template" tiene que ir todo el código HTML-->
  <h1>TemplateComponent.vue</h1>
</template>


<script>
import { store } from "../store.js";

export default {
  // Nombre del componente
  name: "TemplateComponent",
  //Para poder modificar el componente desde un nivel superior, necesitamos que las opciones
  //o propiedades (clases de html) puedan cambiarse desde el html,
  //para ello las declaramos aqui, y eso hace que podamos usarlas en el template/html
  //Ejemplo:escribimos props:["Propname"], que permite acceder desde el compnente superior
  // asi, <TemplateComponent Propname="valor"></>
  props: ["Propname"],

  store,

  mounted() {
    this.$store.watch(
      (state, getters) => getters.GETTERNAME,
      // Nombre del getter sobre el que el watch está escuchando constantemente

      (newValue, oldValue) => {
        if (newValue === "STATEVALUE") {
          //Código javascript de que ocurre cuando el estado es el deseado
        }
      }
    );
  },

  methods: {
    myMethod() {
      //Javasript code
      //Si quieres lanzar una acción, la forma es la siguiente:
      //this.$store.dispatch("actionName", "variable");
    }
  }
};
</script>

<style>
</style>