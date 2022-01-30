<template>
  <div class="card-menu" width="300">
    <v-list>
      <v-list-item-group v-model="selectedItem" color="primary">
        <router-link to="/dashboard" class="text-decoration">
          <v-list-item>
            <v-list-item-title>
              <v-icon>mdi-chart-donut</v-icon>
              <span>Dashboard</span>
            </v-list-item-title>
          </v-list-item>
        </router-link>

        <router-link to="/renda" class="text-decoration">
          <v-list-item>
            <v-list-item-title>
              <v-icon>mdi-account-arrow-up</v-icon>
              <span>Renda</span>
            </v-list-item-title>
          </v-list-item>
        </router-link>

        <router-link to="/renda" class="text-decoration">
          <v-list-item>
            <v-list-item-title>
              <v-icon>mdi-account-arrow-down</v-icon>
              <span>Despesa</span>
            </v-list-item-title>
          </v-list-item>
        </router-link>

        <router-link to="/renda" class="text-decoration">
          <v-list-item>
            <v-list-item-title>
              <v-icon>mdi-bell-ring</v-icon>
              <span>Lembrete</span>
            </v-list-item-title>
          </v-list-item>
        </router-link>
      </v-list-item-group>
    </v-list>
  </div>
</template>

<script>
export default {
  data() {
    return {
      selectedItem: "",
    };
  },

  props: {
    resource: {
      type: Boolean,
    },
  },

  created() {
    this.initialize();
  },

  methods: {
    initialize() {
      let routeName = this.$router.history.current.path;

      if (routeName == "/dashboard") {
        this.selectedItem = 0;
      }

      if (routeName == "/renda") {
        this.selectedItem = 1;
      }
    },
  },
};
</script>

<style>
.card-menu {
  border-radius: 8px;
}

.text-decoration {
  text-decoration: none;
}

.v-list-item {
  margin: 10px 0;
}

.v-list-item__title {
  display: flex;
  align-items: center;
}

.v-list-item__title > .v-icon {
  color: #2c3e50 !important;
  margin-right: 10px;
}

.v-list-item__title > span {
  font-family: "Poppins", sans-serif;
  font-size: 14px;
  font-weight: 500;
  color: #2c3e50 !important;
}

.v-list-item--active {
  border-radius: 8px !important;
  border: 1px solid #3498db !important;
}

.v-sheet.v-list {
  border-radius: 10px;
}
</style>
