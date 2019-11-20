<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png" />
    <h3>Home Value = {{ getHome }}</h3>
  </div>
</template>

<script>
// @ is an alias to /src
import { mapGetters } from "vuex";

export default {
  name: "home",
  computed: {
    ...mapGetters(["getHome"])
  }
};
</script>
