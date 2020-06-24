<template>
  <div class="container">
    RearmMainPanel
    <img src="./../assets/images/blueprints/su25.png" class="aircraftBlueprint" />
    <div class="pylonsContainer" >
      <pylon-selector  v-for="pylon in pylonsList" :key="pylon.index"></pylon-selector>
    </div>
  </div>
</template>

<script>
import PylonSelector from "./PylonSelector";

export default {
  name: "RearmMainPanel",
  components: { PylonSelector },
  data: function() {
    return {
      pylonsList: [
        { index: 1 },
        { index: 2 },
        { index: 3 },
        { index: 4 },
        { index: 5 },
        { index: 6 },
        { index: 7 },
        { index: 8 },
        { index: 9 },
        { index: 10 },
        { index: 11 }
      ]
    };
  }
};
</script>

<style scoped>
.container {
  background-color: darkseagreen;
  grid-area: main;
  min-height: 300px;
}
.pylonsContainer{
    display: flex;
    flex-direction: row;
}
</style>