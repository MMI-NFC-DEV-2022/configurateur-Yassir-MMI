<script setup lang="ts">
import BasketProfil from "../components/BasketProfil.vue";
import type { Basket } from "../types";
const exemples: Basket[] = [{
  semelle: "#FF0000",
  empeigne: "#FFFFFF",
  pointe: "#FFFFFF",
  oeillet: "#FFFFFF",
  bande: "#00FF00",
  languette: "#FFFFFF",
  lacet: "#00FF00",
  trimestre: "#FFFFFF",
},
{
  semelle: "#0000FF",
  empeigne: "#000000",
  pointe: "#000000",
  oeillet: "#000000",
  bande: "#FF0000",
  languette: "#000000",
  lacet: "#FF0000",
  trimestre: "#000000",
},
{
  semelle: "#00FF00",
  empeigne: "#FF0000",
  pointe: "#FF0000",
  oeillet: "#FF0000",
  bande: "#0000FF",
  languette: "#FF0000",
  lacet: "#0000FF",
  trimestre: "#FF0000",
},
{
  semelle: "#FFFFFF",
  empeigne: "#00FF00",
  pointe: "#00FF00",
  oeillet: "#00FF00",
  bande: "#FFFFFF",
  languette: "#00FF00",
  lacet: "#FFFFFF",
  trimestre: "#00FF00",
},
{
  semelle: "#FF00FF",
  empeigne: "#FFFF00",
  pointe: "#FFFF00",
  oeillet: "#FFFF00",
  bande: "#FF00FF",
  languette: "#FFFF00",
  lacet: "#FF00FF",
  trimestre: "#FFFF00",
},

];
</script>
<template>
  <section>
    <h1 class="text-2xl">Exemples de Baskets</h1>
    <div class="flex flex-wrap gap-2">
      <div class="w-64">
        <RouterLink
          v-for="exemple in exemples"
          :to="{
            name: '/basket/exemple/[data]',
            params: { data: JSON.stringify(exemple) },
          }"
        >
          <BasketProfil class="w-64" v-bind="exemple" />
        </RouterLink>
      </div>
    </div>
  </section>
</template>