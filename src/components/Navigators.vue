<template>
    <div>
    <v-navigation-drawer
      v-model="drawer"
      app
      clipped
    >
      <v-list dense>
        <v-list-item link>
          <v-list-item-action>
            <v-icon>mdi-view-dashboard</v-icon>
          </v-list-item-action>
          <v-list-item-content>
            <v-list-item-title>Dashboard</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
        <v-list-item link>
          <v-list-item-action>
            <v-icon>mdi-settings</v-icon>
          </v-list-item-action>
          <v-list-item-content>
            <v-list-item-title>Settings</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
        <router-link id="router" to="/login">
          <v-list-item link>
            <v-list-item-action>
              <v-icon>mdi-login</v-icon>
            </v-list-item-action>
            <v-list-item-content>
              <v-list-item-title>Login/SignUp</v-list-item-title>
            </v-list-item-content>
          </v-list-item>
        </router-link>
         
        
      </v-list>
    </v-navigation-drawer>

    <v-app-bar
      app
      clipped-left
      src="../assets/background.png"
    >
      <v-app-bar-nav-icon
          @click.stop="drawer = !drawer"
          color="#7e6d6d"
      />
        <template v-slot:img="{ props }">
          <v-img
            v-bind="props"
          ></v-img>
        </template>
      <v-img
          alt="smart-kot logo"
          class="shrink mr-2"
          contain
          src="../assets/logo.png"
          transition="scale-transition"
          width="200"
          @click.stop="drawer = !drawer"
        />
        <v-spacer></v-spacer>
        <v-btn icon
          color="#ffffff"
          href="https://github.com/smart-kot"
        >
          <v-icon>mdi-github</v-icon>
        </v-btn>
    </v-app-bar>
    </div>
</template>

<script>
export default {
    data: () => ({
      drawer: null,
    }),
    created () {
      this.$vuetify.theme.dark = false;
    }
}
</script>

<style>
#router {
    text-decoration: none;
    color: #7e6d6d
}

v-app-bar {
    top:0px;
}
</style>