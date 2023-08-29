<template>
  <v-card>
    <v-card-title>Adicionar usuario</v-card-title>
    <v-card-text>
      <v-row>
        <v-col>
          <v-text-field
            label="Nome"
            variant="outlined"
            :rules="nameRules"
          ></v-text-field>
        </v-col>
        <v-col>
          <v-text-field
            label="Email"
            variant="outlined"
            :rules="emailRules"
          ></v-text-field>
        </v-col>
      </v-row>
      <v-select
        label="cargo"
        variant="outlined"
        :items="['admin', 'MARTELADOR', 'MATADOR']"
      ></v-select>
    </v-card-text>
    <v-card-actions>
      <v-btn variant="text" @click="$emit('close-create-user-form')">
        cancelar
      </v-btn>
      <v-spacer></v-spacer>
      <v-btn variant="tonal" color="success">Salvar</v-btn>
    </v-card-actions>
  </v-card>
</template>

<script setup lang="ts">
defineEmits(["close-create-user-form"]);

const emailRules: ReadonlyArray<(value: String) => string | true> = [
  (value) => {
    if (value) return true;

    return "O email é obrigatório";
  },
  (value) => {
    if (value.includes("@") && value.includes(".")) return true;
    return "email invalido";
  },
];

const nameRules: ReadonlyArray<(value: String) => string | true> = [
  (value) => {
    if (value) return true;

    return "O Nome é obrigatório";
  },
  (value) => {
    if (value.match(/[a-zA-Z]/)) return true;
    return "Nome só pode ter letras";
  },
];
</script>

<style></style>
