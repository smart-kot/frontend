<template>
  <div class="login">
    <v-row
    full-width
    justify="center"
    
    >
      <v-col 
        xs="12"
        sm="12"
        md="2"
      ></v-col>
      <v-col
        xs="12"
        sm="8"
        md="4"
      >
        <v-card
          class="mx-auto justify-center"
          
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
            <v-text-field
              v-model="inputLogin.username"
              label="Username"
            ></v-text-field>
            <v-text-field
              v-model="inputLogin.password"
              :append-icon="showLoginPasswd ? 'mdi-eye' : 'mdi-eye-off'"
              :rules="[rules.required]"
              :type="showLoginPasswd ? 'text' : 'password'"
              name="input-10-1"
              label="Password"
              @click:append="showLoginPasswd = !showLoginPasswd"
            ></v-text-field>
            <v-btn class="ma-2" outlined color="#ff6200">Login</v-btn>
          </v-card-text>
        </v-card>
        
      </v-col>
      <v-col
        xs="12"
        sm="8"
        md="4"
      >
        <v-card
          class="mx-auto justify-center"
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
            <v-text-field
              v-model="inputSignUp.firstName"
              label="First Name"
            ></v-text-field>
            <v-text-field
              v-model="inputSignUp.lastName"
              label="Last Name"
            ></v-text-field>
            <v-text-field
              v-model="inputSignUp.username"
              label="Username"
            ></v-text-field>
            <v-text-field
              v-model="inputSignUp.email"
              label="E-mail"
            ></v-text-field>
            <v-text-field
              v-model="inputSignUp.password"
              :append-icon="showSignUpPasswd ? 'mdi-eye' : 'mdi-eye-off'"
              :rules="[rules.required, rules.min]"
              :type="showPasswd ? 'text' : 'password'"
              name="input-10-1"
              label="Password"
              hint="At least 10 characters"
              counter
              @click:append="showSignUpPasswd = !showSignUpPasswd"
            ></v-text-field>
            <v-text-field
              v-model="inputSignUp.passwdConf"
              :append-icon="showSignUpPasswdConf ? 'mdi-eye' : 'mdi-eye-off'"
              :type="showSignUpPasswdConf ? 'text' : 'password'"
              :rules="[rules.passwdMatch]"
              name="input-10-1"
              label="Confirm Password"
              error="this.error"
              @click:append="showSignUpPasswdConf = !showSignUpPasswdConf"
            ></v-text-field>
            <v-btn class="ma-2" outlined color="#ff6200">Sign Up</v-btn>
          </v-card-text>
        </v-card>
      </v-col>
      <v-col
        xs="12"
        sm="12"
        md="2"
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
  },
  data () {
    return {
      error: false,
      showLoginPasswd: false,
      showSignUpPasswd: false,
      showSignUpPasswdConf: false,
      rules: {
        required: value => !!value || 'Required.',
        passwdMatch: () => this.input.password === this.input.passwdConf || ('The passwords you entered don\'t match' && this.error == true),
      },
      inputSignUp: {
        firstName: '',
        lastName: '',
        username: '',
        email: '',
        password: '',
        passwdConf: ''
      },
      inputLogin: {
        username: '',
        password: ''
      },
    }
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
