<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png" />
    <h3>About Value = {{ getAbout }}</h3>
  </div>
</template>

<script>
// @ is an alias to /src
import { mapGetters } from "vuex";

export default {
  name: "about",
  computed: {
    ...mapGetters(["getAbout"])
  }
};
</script>
