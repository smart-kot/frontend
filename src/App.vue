
<template>
  <v-app id="inspire">
    <v-system-bar dark color="#ff6300"></v-system-bar>
    <Navigators />

    <v-content>
      <v-container
        class="fill-height"
        fluid
      >
        <router-view />
      </v-container>
    </v-content>

    <v-footer app>
      <span>&copy; Smart-kot 2019</span>
    </v-footer>
  </v-app>
</template>

<script>
import Navigators from './components/Navigators'
  export default {
    components : {
      Navigators
    }
  }
</script>

<style>

router-link{
    text-decoration: none;
}

</style>