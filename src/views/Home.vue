<template>
  <div class="home">
    <v-img
          :src="require('../assets/logo.svg')"
          class="my-3"
          contain
          height="200"
    />
    <v-card>
      <div id="cardContent">
        <h1>Welcome @ Smart-kot</h1>
        <p>Smart-kot is a full automation and controllable platform to control your home. 
          that's exactly where the name 'Smart-kot' comes from.
        </p>
      </div>
      
    </v-card>
    
  </div>
</template>

<script>
// @ is an alias to /src

export default {
  name: 'Home',
  components: {
  }
}
</script>

<style scoped>
  h1, p {
    color: #7e6d6d
  }

  #cardContent {
    padding: 20px;
  }
</style>
