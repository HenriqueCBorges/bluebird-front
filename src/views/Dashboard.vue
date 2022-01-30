<template>
  <div>
    <Navbar />
    <v-main class="main">
      <v-container>
        <v-row>
          <v-col cols="2">
            <Sidebar />
          </v-col>
          <v-col>
            <Dashboard />
          </v-col>
        </v-row>
      </v-container>
    </v-main>
  </div>
</template>

<script>
import Navbar from "../components/Navbar-comp.vue";
import Sidebar from "../components/Sidebar-comp.vue";
import Dashboard from "../components/dashboard/Dashboard-comp.vue";
export default {
  components: {
    Navbar,
    Sidebar,
    Dashboard,
  },
  data: () => ({}),
};
</script>

<style></style>