<template>
  <div class="add-card">
    <p>Add new topic</p>
  </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({
  name: "AddCard",
  props: {
    topic: String,
  },
});
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
.add-card {
  background-color: rgba(134, 174, 255, 0.5);
  color: #fff;
  border-color: var(--pros-light);
  box-shadow: 0px 0px 10px -11px;
  border-radius: 10px;
  text-align: left;
  padding: 0.2em 1em;
  margin: 0.5em 1em;
  border-style: dashed;
  text-align: center;
}
</style>
