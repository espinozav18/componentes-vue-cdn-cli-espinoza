<template>
  <v-col cols="12" :lg="mostrar" :md="mostrar">
    <v-card>
      <v-card-title>{{ titulo }}</v-card-title>
      <v-card-text>
           </v-card-text>
    </v-card>
  </v-col>
</template>

<script>
export default {
  name: "CardVue",
  props: {
    titulo: { type: String, default: "" },
    mostrar: { type: Number, default: 6 },
  },
};
</script>

<style lang="scss" scoped>
</style>