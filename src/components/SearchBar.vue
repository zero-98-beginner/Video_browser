<template>
  <div>
    <input @keyup.enter="onInput" />
  </div>
</template>

<script>
import { defineComponent } from "vue";

export default defineComponent({
  name: "SearchBar",
  methods: {
    onInput(event) {
      this.$emit("termChange", event.target.value);
    },
  },
});
</script>


<style scoped>
input {
  width: 75%;
}

div {
  text-align: center;
  margin: 20px;
}
</style>
