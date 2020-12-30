<template>
  <div class="home">
    <div class="container">
      <v-spinners class="spinners"></v-spinners>
    </div>
  </div>
</template>

<script>
import VSpinners from '../../packages/src/index';
export default {
  name: "Home",
  components: {
    VSpinners
  }
};
</script>
<style lang="less" scoped>
h1 {
  margin: 0;
}
.container {

  .spinners {
    margin:0 auto;
  }
}
</style>