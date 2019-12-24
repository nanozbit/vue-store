<template>
  <v-footer dark padless>
    <v-card class="flex" flat tile>
      <v-card-title class="purple darken-4 d-flex justify-center">
        <strong class="subheading text-center "
          >Conectate a nuestra redes sociales</strong
        >
      </v-card-title>

      <v-card-text class="py-2 white--text text-center">
        {{ new Date().getFullYear() }} — <strong>Guayaquil-Ecuador</strong>
      </v-card-text>
    </v-card>
  </v-footer>
</template>

<script>
export default {
  name: "Footer"
};
</script>

<style scoped></style>
