<template>
  <div class="container">
    <div class="row">
      <div class="col-xs-12">
        <br />
        <button class="btn btn-primary" @click="selectedTemplate = 'appBlue'">Load Blue Template</button>
        <button class="btn btn-success" @click="selectedTemplate = 'appGreen'">Load Green Template</button>
        <button class="btn btn-danger" @click="selectedTemplate = 'appRed'">Load Red Template</button>
        <hr />
        <component :is="selectedTemplate"></component>
      </div>
    </div>
  </div>
</template>

<script>
import Blue from "./components/Blue";
import Green from "./components/Green";
import Red from "./components/Red";

export default {
  components: {
    appBlue: Blue,
    appGreen: Green,
    appRed: Red,
  },
  data() {
    return {
      selectedTemplate: "appBlue",
    };
  },
};
</script>

<style>
</style>

