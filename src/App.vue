<template>
  <v-app>
    <router-view/>
  </v-app>
</template>

<script>

export default {
  name: 'App',

  data: () => ({
    //
  }),
};
</script>

<style>
.main {
  height: 100vh;
  background-color: #25252507;
}

.section {
  background-color: white;
  border-radius: 10px;
  padding: 25px;
}

.header {
  font-family: "Poppins", sans-serif;
  font-size: 14px;
  font-weight: 500;
}
</style>
