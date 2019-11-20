<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png" />
    <h4>Possible components: "polygon", "square", "triangle"</h4>
    <input type="text" v-model="inputValue" />
    <component :is="shape"></component>
  </div>
</template>

<script>
// @ is an alias to /src

export default {
  name: "home",
  components: {
    squareShape: () => import("../components/squareShape"),
    triangleShape: () => import("../components/triangleShape"),
    polygonShape: () => import("../components/polygonShape")
  },
  data() {
    return {
      val: "",
      shape: ""
    };
  },
  computed: {
    inputValue: {
      get() {
        return this.val;
      },
      set(value) {
        this.val = value;
        switch (value) {
          case "polygon":
            this.shape = "polygonShape";
            break;

          case "square":
            this.shape = "squareShape";
            break;

          case "triangle":
            this.shape = "triangleShape";
            break;

          default:
            break;
        }
      }
    }
  }
};
</script>
<style lang="scss" scoped>
.home {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;

  & input {
    margin-top: 2rem;
  }
}
</style>
