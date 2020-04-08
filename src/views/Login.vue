<template>
  <div class="login">
    <v-row
    full-width
    justify="center"
    
    >
      <v-col 
        xs="0"
        sm="0"
        md="12"
      ></v-col>
      <v-col
        xs="12"
        sm="8"
        md="4"
      >
        <v-card
          class="mx-auto text-left"
        >
          <v-img
            class="align-end"
            height="70px"
            src="../assets/background_half_left_shift.png"
          >
            <v-card-title 
              id="login"
            >
            Login
            </v-card-title>
          </v-img>
          <v-card-text>
            Login
          </v-card-text>
        </v-card>
        
      </v-col>
      <v-col
        xs="12"
        sm="8"
        md="4"
      >
        <v-card
          class="mx-auto text-left"
        >
          <v-img
            class="align-end"
            height="70px"
            src="../assets/background_half_left.png"
          >
            <v-card-title 
              id="signUp"
            >
              Sign Up
            </v-card-title>
          </v-img>
          <v-card-text>
            Login
          </v-card-text>
        </v-card>
      </v-col>
      <v-col
        xs="0"
        sm="0"
        md="12"
      >
      </v-col>
    </v-row>
  </div>
</template>

<script>
// @ is an alias to /src

export default {
  name: 'login',
  components: {
  }
}
</script>

<style scoped>
  h1, p {
    color: #7e6d6d
  }

  #login {
    color: #ffffff
  }

  #signUp {
    color: #ffffff
  }
</style>
