<script lang="ts">

import Notes from './components/Notes.vue'
import BarPlot from './components/BarPlot.vue'
import RadialPlot from './components/RadialPlot.vue'
import ScatterPlot from './components/ScatterPlot.vue'
/*
import Example from './components/Example.vue'
import ExampleWithLegend from './components/ExampleWithLegend.vue';
import ExampleWithInteractions from './components/ExampleWithInteractions.vue';
*/

export default {
  components: {
    Notes,
    BarPlot,
    RadialPlot,
    ScatterPlot
    /*
    Example,
    ExampleWithLegend,
    ExampleWithInteractions
    */
  }
};

</script>

<!--This is using the grid component from Vuetify to do layout design-->
<template>
  <v-container id="main-container" class="d-flex flex-column flex-nowrap" fluid>
    <v-row no-gutters>
      <v-col class="barplot-col" cols="8">
        <BarPlot />
      </v-col>
      <v-col class="starplot-col" cols="3.7">
        <RadialPlot />
      </v-col>
    </v-row>
    <v-row class="scatterplot-row" rows="3">
      <v-col cols="11.5">
        <ScatterPlot />
      </v-col>
    </v-row>
  </v-container>
</template>

<style scoped>
#main-container {
  height: 100vh;
}

.barplot-col,
.starplot-col,
.scatterplot-col {
  height: 60vh;
  width: 100vw;
  margin: 0.5rem;
  border: 2px solid black;
}
.scatterplot-row{
  height: 33vh;
  width: 100vw - 500;
  margin: 0.3rem;
  border: 2px solid;
}
</style>