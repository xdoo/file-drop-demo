<template>
  <v-container fluid fill-height>
    <v-row class="text-center">
      <v-col cols="12">
         <input 
      type="file" 
      id="fileUpload" 
      accept="text/xml" 
      style="display:none">
    <v-sheet
      ref="dropzone"
      id="dropzone"
      title="Click to select a file from your computer."
      color="black"
      width="100%"
      style="cursor:pointer;border-style: solid;border-width: 4px;border-color: green;"
      height="250"
    >
      <v-col class="white--text">
          <v-row justify="center" v-if="!loading">
            <v-icon
              v-if="!dragover" 
              color="white" 
              size="120"
              >mdi-cloud-upload-outline</v-icon>
            <v-icon
              v-if="dragover" 
              color="white" 
              size="120"
              >mdi-book-plus</v-icon>
          </v-row>
          <v-row justify="center" v-if="!loading">
            <span>Select or drop your file here!</span>
          </v-row>
          <v-row justify="center" v-if="loading">
            <v-progress-circular
              size="60"
              width="15"
              color="white"
              indeterminate
            ></v-progress-circular>
          </v-row>
          <v-row justify="center" v-if="loading">
            <span >Datei wird verarbeitet</span>
          </v-row>
        </v-col>
    </v-sheet>
      </v-col>
    </v-row>
  </v-container>
</template>

<script lang="ts">
  import Vue from "vue"
  import { Component } from "vue-property-decorator"

  @Component
  export default class FileDrop extends Vue {
    loading: boolean = false
    dragover: boolean = false
  }
</script>
