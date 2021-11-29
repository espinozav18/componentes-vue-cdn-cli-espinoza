<template>
  <v-img
    alt="Vuetify Logo"
    class="shrink mr-2"
    contain
    :src="src"
    transition="scale-transition"
    :style="estilo"
  />
</template>

<script>
export default {
  name: "Atitulo",
  props: {
    alt: { type: String },
    src: { type: String },
    estilo: { type: Array },
  },
};
</script>

<style lang="scss" scoped>
</style>
