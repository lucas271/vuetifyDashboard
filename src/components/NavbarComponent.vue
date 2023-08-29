<template>
  <v-app-bar flat class="border-b elevation-1">
    <v-app-bar-nav-icon
      @click="$emit('isDrawerOpenChange')"
    ></v-app-bar-nav-icon>
    <v-app-bar-title>Meu app</v-app-bar-title>

    <template #append>
      <v-switch
        color="indigo-darken-3"
        :model-value="isDarkMode"
        @click="$emit('switchTheme')"
        :hide-details="true"
      ></v-switch>

      <v-btn icon class="mr-2">
        <v-badge dot color="info">
          <v-icon icon="mdi-bell-outline"></v-icon>
        </v-badge>
      </v-btn>

      <v-menu>
        <template #activator="{ props }">
          <v-avatar class="scale2" v-bind="props">
            <v-img
              class="scale3"
              cover
              src="https://images.unsplash.com/photo-1575936123452-b67c3203c357?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxzZWFyY2h8Mnx8aW1hZ2V8ZW58MHx8MHx8fDA%3D&w=1000&q=80"
            ></v-img>
          </v-avatar>
        </template>
        <v-card min-width="200px">
          <v-list :lines="false" density="compact" nav>
            <v-list-item prepend-icon="mdi-account-outline">
              <v-list-item-title>Meu perfil</v-list-item-title>
            </v-list-item>
            <v-list-item prepend-icon="mdi-heart-outline">
              <v-list-item-title>Favoritos </v-list-item-title>
            </v-list-item>
          </v-list>
        </v-card>
      </v-menu>
    </template>
  </v-app-bar>
</template>
<script setup lang="ts">
defineProps({
  isDrawerOpen: {
    type: Boolean,
    required: true,
  },
  isDarkMode: {
    type: Boolean,
    required: true,
  },
});

defineEmits(["isDrawerOpenChange", "switchTheme"]);
</script>
<style></style>
