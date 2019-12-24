<template>
  <v-card class="mx-auto" max-width="300">
    <v-img :src="item.photo" height="200px"></v-img>

    <v-card-title>
      {{ item.name }}
    </v-card-title>

    <v-card-subtitle>
      1,000 miles of wonder
    </v-card-subtitle>

    <v-card-actions>
      <v-btn text>Compartir</v-btn>

      <v-btn color="purple" text>
        Explorar
      </v-btn>

      <v-spacer></v-spacer>

      <v-btn icon @click="show = !show">
        <v-icon>{{ show ? "mdi-chevron-up" : "mdi-chevron-down" }}</v-icon>
      </v-btn>
    </v-card-actions>

    <v-expand-transition>
      <div v-show="show">
        <v-divider></v-divider>

        <v-card-text>
          {{ item.description }}
        </v-card-text>
      </div>
    </v-expand-transition>
  </v-card>
</template>

<script>
export default {
  name: "ArticleList",
  props: ["item"],
  data: () => ({
    show: false
  })
};
</script>

<style scoped></style>
