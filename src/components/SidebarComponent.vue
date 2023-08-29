<template>
  <v-navigation-drawer>
    <v-list>
      <v-list-subheader>Menu</v-list-subheader>
      <v-list-item prepend-icon="mdi-home">Home</v-list-item>
      <v-list-item prepend-icon="mdi-account">Usuários</v-list-item>
      <v-list-group value="Clientes">
        <template #activator="{ props }">
          <v-list-item v-bind="props" prepend-icon="mdi-account-circle">
            Clientes</v-list-item
          >
        </template>

        <v-list-item prepend-icon="mdi-currency-usd">Faturamento</v-list-item>
        <v-list-item prepend-icon="mdi-chart-line">Relatorio</v-list-item>
      </v-list-group>
    </v-list>
  </v-navigation-drawer>
</template>

<script setup lang="ts"></script>

<style></style>
