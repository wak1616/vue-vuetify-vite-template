<script setup>
import { ref } from 'vue';

const title = ref('Vue + Vuetify + Vite Template');
const message = ref('Ready to build your app!');
</script>

<template>
  <v-app>
    <v-app-bar color="primary" height="72">
      <v-container class="d-flex align-center">
        <v-app-bar-title class="app-title">{{ title }}</v-app-bar-title>
      </v-container>
    </v-app-bar>

    <v-main>
      <v-container>
        <v-row class="mt-4">
          <v-col cols="12">
            <v-card>
              <v-card-title class="text-h5">Welcome to Your New Project</v-card-title>
              <v-card-text>
                <p class="text-body-1">
                  This is a template project with Vue 3, Vuetify, and Vite already configured.
                  Edit <code>src/App.vue</code> to customize this page.
                </p>
                <v-alert
                  color="info"
                  variant="tonal"
                  class="mt-4"
                >
                  {{ message }}
                </v-alert>
              </v-card-text>
              <v-card-actions>
                <v-spacer></v-spacer>
                <v-btn
                  color="primary"
                  @click="message = 'You clicked the button!'"
                >
                  Click Me
                </v-btn>
              </v-card-actions>
            </v-card>
          </v-col>
        </v-row>
      </v-container>
    </v-main>

    <v-footer app class="bg-secondary">
      <v-container>
        <div class="text-center text-body-2">
          &copy; {{ new Date().getFullYear() }} — <strong>Vue Vuetify Template</strong>
        </div>
      </v-container>
    </v-footer>
  </v-app>
</template>

<style>
.app-title {
  font-size: 1.5rem;
  line-height: 2rem;
  font-weight: 500;
}

@media (max-width: 600px) {
  .app-title {
    font-size: 1.2rem;
    line-height: 1.8rem;
  }
}
</style>
