<template>
  <v-app>
    <Navbar />
    <Articles :listArt="listArt" />
    <Footer />
  </v-app>
</template>

<script>
// components
import Navbar from "./components/Navbar";
import Footer from "./components/Footer";
import Articles from "./components/Articles";
// firebase
import firebase from "firebase/app";
import "firebase/firestore";
import config from "./config";

const app = firebase.initializeApp(config);
const db = app.firestore();
const articleCol = db.collection("article");
export default {
  name: "App",
  firestore: {
    listArt: articleCol
  },
  mounted() {},

  components: {
    Navbar,
    Footer,
    Articles
  }
};
</script>

<style scoped></style>
