<template>
  <div>
    <v-container fluid>
      <v-layout>
        <v-row no-gutters>
          <div v-for="item in art" :key="item.id">
            <v-col>
              <ArticleList :item="item" />
            </v-col>
          </div>
        </v-row>
      </v-layout>
    </v-container>
  </div>
</template>

<script>
import ArticleList from "./ArticleList";

export default {
  name: "Articles",
  props: ["listArt"],
  data() {
    return {
      art: this.listArt
    };
  },
  components: {
    ArticleList
  }
};
</script>

<style scoped></style>
