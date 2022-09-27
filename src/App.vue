<template>
  <v-app id="inspire">
    <v-system-bar app>
      <v-spacer></v-spacer>
       <!-- <v-icon class="mr-3">mdi-account</v-icon>
        <v-list-item-title>Mi perfil</v-list-item-title>-->
    </v-system-bar>

    <v-app-bar app class="grey lighten-3">
      <v-app-bar-nav-icon @click="drawer = !drawer"></v-app-bar-nav-icon>
      <v-avatar class="ml-3">
        <img src="./assets/rey-salomon.jpg">
      </v-avatar>

      <v-toolbar-title class="ml-3">El rey Salomón</v-toolbar-title>
    </v-app-bar>

    <v-navigation-drawer v-model="drawer" fixed temporary>
      <v-list>
        <v-list-item @click="method">
          <v-icon class="mr-3">mdi-account-plus-outline</v-icon>
          <v-list-item-title>Registro</v-list-item-title>
        </v-list-item>

        <v-list-item @click="method">
          <v-icon class="mr-3">mdi-login</v-icon>
          <v-list-item-title>Inicio de sesión</v-list-item-title>
        </v-list-item>

        <v-list-item @click="method">
        <v-icon class="mr-3">mdi-account</v-icon>
        <v-list-item-title>Mi perfil</v-list-item-title>
        </v-list-item>

        <!--<v-list-item disabled>
          <v-list-item-title>Option 3</v-list-item-title>
        </v-list-item>-->
      </v-list>
      <!--  -->
    </v-navigation-drawer>

    <v-main class="grey lighten-2">
      <v-container>
        <v-row>
          <template v-for="n in 4">
            <v-col :key="n" class="mt-2" cols="12">
              <strong>Category {{ n }}</strong>
            </v-col>

            <v-col v-for="j in 6" :key="`${n}${j}`" cols="6" md="2">
              <v-sheet height="150"></v-sheet>
            </v-col>
          </template>
        </v-row>
      </v-container>
    </v-main>
  </v-app>
</template>

<script>
export default {
  name: 'App',
  data: () => ({ drawer: null })
}
</script>
