<template>
  <v-app :theme="isDarkMode ? 'dark' : 'light'">
    <v-col>
      <Sidebar v-model="isDrawerOpen" :isDrawerOpen="isDrawerOpen" />
      <Navbar
        :isDrawerOpen="isDrawerOpen"
        :isDarkMode="isDarkMode"
        @isDrawerOpenChange="isDrawerOpen = !isDrawerOpen"
        @switchTheme="isDarkMode = !isDarkMode"
      />
      <v-main>
        <v-container>
          <h1>Dashboard {{ String(isDarkMode) }}</h1>
          <v-row class="ma-2">
            <v-col cols="12">
              <DashboardComponent />
            </v-col>
          </v-row>
          <v-row class="mt-2">
            <ItemsComponent />
          </v-row>
        </v-container>
      </v-main>
    </v-col>
  </v-app>
</template>

<script setup lang="ts">
import { ref } from "vue";
import Sidebar from "./components/SidebarComponent.vue";
import Navbar from "./components/NavbarComponent.vue";
import DashboardComponent from "./components/DashboardComponent.vue";
import ItemsComponent from "./components/ItemsComponent.vue";

const isDrawerOpen = ref<boolean>(false);
const isDarkMode = ref<boolean>(false);
</script>

<style>
.scale:hover {
  transition-duration: 350ms;
  transform-origin: center;
  transform: scale(1.015);
}

.scale2:hover {
  cursor: pointer;
  transition-duration: 350ms;
  transform-origin: center;
  transform: scale(1.09);
}

.scale3:hover {
  cursor: pointer;
  transition-duration: 350ms;
  transform-origin: center;
  transform: scale(1.115);
}
</style>
