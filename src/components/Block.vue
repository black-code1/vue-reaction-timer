<template>
  <div class="block" v-if="showBlock">click me</div>
</template>

<script>
export default {
  // props i want to receive
  props: ["delay"],
  data() {
    return {
      showBlock: false,
    };
  },
  mounted() {
    console.log("components mounted");
    setTimeout(() => {
      this.showBlock = true;
      console.log(this.delay);
    }, this.delay);
  },
  updated() {
    console.log("components updated");
  },
  unmounted() {
    console.log("unmounted");
  },
};
</script>

<style>
.block {
  width: 400px;
  border-radius: 20px;
  background: #0faf87;
  color: white;
  text-align: center;
  padding: 100px 0;
  margin: 40px auto;
}
</style>
