<template>
  <v-card flat class="w-100%">
    <div class="d-flex justify-space-between">
      <v-card-title>Ultimos usuários</v-card-title>
      <v-card-title>
        <v-btn variant="tonal" size="small" @click="isDialogOpen = true">
          Adicionar usuário
        </v-btn>
        <v-dialog
          v-model="isDialogOpen"
          width="600px"
          height="auto"
          transition="dialog-bottom-transition"
        >
          <CreateUserFormComponent
            @close-create-user-form="isDialogOpen = false"
          />
        </v-dialog>
      </v-card-title>
    </div>

    <v-table flat>
      <thead>
        <tr>
          <th>nome</th>
          <th>email</th>
          <th>cargo</th>
          <th>Ações</th>
        </tr>
      </thead>
      <tbody>
        <tr class="pa-3">
          <td>Fulano</td>
          <td>fulano@gmail.com</td>
          <td>
            <v-chip variant="outlined" color="primary" size="small">
              matador
            </v-chip>
          </td>
          <td>
            <v-btn variant="tonal" color="red-darken-4" :ripple="false">
              Editar
            </v-btn>
          </td>
        </tr>
        <tr>
          <td>Fulaninho</td>
          <td>fulaninho@gmail.com</td>
          <td>
            <v-chip variant="outlined" color="success" size="small">
              salvador
            </v-chip>
          </td>
          <td>
            <v-btn variant="tonal" color="primary">Editar</v-btn>
          </td>
        </tr>
      </tbody>
    </v-table>
  </v-card>
</template>
<script lang="ts" setup>
import { ref } from "vue";
import CreateUserFormComponent from "./CreateUserFormComponent.vue";
const isDialogOpen = ref(false);
</script>
<style></style>
