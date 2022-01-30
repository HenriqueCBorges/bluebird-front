<template>
  <v-app-bar class="navbar" color="white" flat>
    <v-container class="py-0 fill-height">
      <img class="logo-img" src="../assets/logo-bb-icon.png" alt="" />

      <v-spacer></v-spacer>

      <div class="text-center">
        <v-menu min-width="250px">
          <template v-slot:activator="{ on, attrs }">
            <v-avatar color="blue" size="36" v-bind="attrs" v-on="on">
              <span class="white--text text-h6">B</span>
            </v-avatar>
          </template>

          <v-card>
            <v-list-item-content class="justify-center">
              <div class="mx-auto text-center">
                <v-avatar color="blue" size="46" class="mb-2">
                  <span class="white--text text-h5">{{ user.initials }}</span>
                </v-avatar>

                <h3>{{ user.fullName }}</h3>
                <p class="text-caption mt-1">
                  {{ user.email }}
                </p>
                <v-divider class="my-3"></v-divider>
                <v-btn depressed rounded text> Minha Conta </v-btn>
                <v-divider class="my-3"></v-divider>
                <v-btn depressed rounded text> Desconectar </v-btn>
              </div>
            </v-list-item-content>
          </v-card>
        </v-menu>
      </div>
    </v-container>
  </v-app-bar>
</template>

<script>
export default {
  data: () => ({
    user: {
      initials: "B",
      fullName: "BlueBird",
      email: "bluebird.desenv@email.com.br",
    },
  }),
};
</script>

<style></style>
