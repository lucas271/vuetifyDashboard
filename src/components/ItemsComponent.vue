<template>
  <v-col
    cols="12"
    sm="6"
    md="4"
    lg="3"
    class="scale"
    v-for="item in [1, 2, 3, 4]"
  >
    <v-card class="scale">
      <v-img
        class="align-end text-white"
        src="https://images.pexels.com/photos/17987435/pexels-photo-17987435/free-photo-of-vicuna-en-la-puna.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=1"
        cover
        ><v-card-title> Top 10 paraísos deserticos </v-card-title>
      </v-img>
      <v-card-subtitle class="pt-3">Egito - 10</v-card-subtitle>
      <v-card-text>
        <div>Piramides do egito</div>
        <div>Muitos camelos andam lá</div>

        <v-card-actions>
          <v-btn variant="outlined" color="primary">Ver mais</v-btn>
          <v-btn prepend-icon="mdi-cart" variant="tonal" color="blue"
            >Comprar</v-btn
          >
        </v-card-actions>
      </v-card-text>
    </v-card>
  </v-col>
</template>

<script setup lang="ts"></script>

<style></style>
