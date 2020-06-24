<template>
  <div class="rearm-container">
    Rearm
    <rearm-main-panel></rearm-main-panel>
    <rearm-auxiliary-panel></rearm-auxiliary-panel>
    <stats-summary></stats-summary>
  </div>
</template>

<script>
import RearmAuxiliaryPanel from "./RearmAuxiliaryPanel.vue";
import RearmMainPanel from "./RearmMainPanel.vue";
import StatsSummary from "./StatsSummary.vue";

export default {
  name: "Rearm",

  components: {
    RearmMainPanel,
    RearmAuxiliaryPanel,
    StatsSummary
  }
};
</script>

<style scoped>
.rearm-container {
  background-color: lime;
  padding: 5px;
  display: grid;
  grid-gap: 5px;
  grid-template-rows: [summary-panel] 1fr [rearm-panel] 3fr;
  grid-template-columns: 2fr 1fr;
  grid-template-areas:
    "stats stats"
    "main auxiliary"
}
</style>