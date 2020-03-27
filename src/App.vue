<template>
  <v-app>
    <v-app-bar
      app
      color="black"
      dark
    >
      <div class="d-flex align-center">
        <span class="headline font-weight-black">FileDrop</span><span class="headline font-weight-light">Demo</span>
      </div>

      <v-spacer></v-spacer>
    </v-app-bar>

    <v-content>
      <file-drop/>
    </v-content>
  </v-app>
</template>

<script lang="ts">
import Vue from 'vue';
import FileDrop from './components/FileDrop.vue';

export default Vue.extend({
  name: 'App',

  components: {
    FileDrop,
  },

  data: () => ({
    //
  }),
});
</script>
