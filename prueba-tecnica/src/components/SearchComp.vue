<template>
    <v-app-bar app color="rgb(138, 43, 226)" dark>
      <v-toolbar-title>Prueba Vue</v-toolbar-title>
      <v-spacer></v-spacer>
      <v-btn class="btn-space" color="white"><span>Login</span></v-btn>
      <v-btn color="white"><span>Get Started</span></v-btn>
    </v-app-bar>
  </template>
  
  <script>
  export default {
    name: "SearchComp",
    data: () => ({
      //
    }),
  };
  </script>

  <style>
  span{
    color: rgb(138, 43, 226)
  }
  .btn-space{
    margin-right: 5px;
    margin-left: 5px;
  }
</style>