<template>
  <div class="tray-name" @click="handleClick">{{ data.name }}</div>
</template>

<script>
import { mapMutations } from "vuex";

export default {
  name: "TrayName",
  props: ["data"],
  methods: {
    ...mapMutations(["setSelectTray"]),
    handleClick() {
      this.setSelectTray(this.data);
    },
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.tray-name {
  cursor: pointer;
  user-select: none;
  text-align: center;
}
.tray-name:active {
  background-color: yellow;
}
</style>
