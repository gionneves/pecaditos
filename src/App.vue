<template>
  <Header></Header>
  <Posts :posts="posts"></Posts>
  <Footer></Footer>
</template>

<script lang="ts">
import { Options, Vue } from "vue-class-component";
import Header from "./components/Header.vue";
import Footer from "./components/Footer.vue";
import Posts from "./components/Comments.vue";

@Options({
  components: {
    Header,
    Footer,
    Posts,
  },

  data() {
    posts: [];
  },
  created() {
    this.posts = [
      {
        id: 1,
        text: "Fora bolsonaro!",
      },
      {
        id: 2,
        text: "Eu acho isso muita falta de sacanagem como pode uma mulher n sofrer com isso mt putaria essa merda hein",
      },
      {
        id: 3,
        text: "Vai se lascar moleque burro da porra mano",
      },
    ];
  },
})
export default class App extends Vue {}
</script>

<style>
@import "https://cdn.jsdelivr.net/npm/bulma@0.9.2/css/bulma.min.css";
</style>
