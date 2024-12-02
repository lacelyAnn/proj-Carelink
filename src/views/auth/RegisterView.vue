<script setup>

import { useDisplay } from 'vuetify'

  const { mobile } = useDisplay()

// import { ref } from 'vue'

// const theme = ref('light')

// function onClick() {
//   theme.value = theme.value === 'light' ? 'dark' : 'light'
// }
</script>

<template>
  <v-responsive class="border rounded">
    <v-app :theme="theme">
      <v-app-bar class="px-3" color="green-darken-1">
        <v-spacer></v-spacer>

         <!-- <v-btn
          :prepend-icon="theme === 'light' ? 'mdi-weather-sunny' : 'mdi-weather-night'"
          text="Toggle Theme"
          slim
          @click="onClick"
        ></v-btn> -->
      </v-app-bar>

      <v-main>
        <v-container>
          <v-row>
            <v-col cols="8" md="5" class="mx-auto">
          <v-card
            class="mx-auto" color="#DCEFC8"
            elevation="24">

          <v-card-title class="text-center">
            <v-img class="mx-auto" src="/logo.webp" :width=" mobile ? '75%' : '25%' "></v-img>
              <h1 class="font-weight-black text-center">CareLink</h1>
              <p class="font-weight-black"> <h6>Register Page</h6> </p>

              <v-divider class="my-1"></v-divider>
            </v-card-title>

            <v-card-text class="bg-surface-dark pt-4">
                  <v-form fast-fail @submit.prevent>
                    <v-text-field
                      label="Full Name:"
                      prepend-icon="mdi-account"
                      variant="outlined"
                    ></v-text-field>

                    <v-text-field
                      label="ID-Number"
                      prepend-icon="mdi-card"
                      variant="outlined"
                    ></v-text-field>

                    <v-text-field
                      label="Email"
                      prepend-icon="mdi-email"
                      variant="outlined"
                    ></v-text-field>

                    <v-text-field
                      label="Password:"
                      type="password"
                      prepend-icon="mdi-lock"
                      variant="outlined"
                    ></v-text-field>

                    <v-text-field
                      label="Confirm Password:"
                      type="password"
                      prepend-icon="mdi-lock"
                      variant="outlined"
                    ></v-text-field>

                    <v-btn class="mt-2" type="submit" prepend-icon="mdi-account-plus" block>Register</v-btn>
                  </v-form>

                  <v-divider class="my-5"></v-divider>
              <h5 class="text-center">
                Already have an account?
                <RouterLink to="login">Click here to Login</RouterLink>
              </h5>
            </v-card-text>
              </v-card></v-col
            >
          </v-row>
        </v-container>
      </v-main>

      <v-footer border app color="green-darken-4">CSU CARELINK 2024</v-footer>
    </v-app>
  </v-responsive>
</template>
