<template>
  <div class="experiment">
    <div class="demo1">
      <v-spinners></v-spinners>
    </div>
  </div>
</template>
<script>
// @ is an alias to /src
import { Spinners } from '../../plugin/v-spinners.umd';
import '../../plugin/v-spinners.css';

export default {
  name: 'experiment',
  components: {
    VSpinners: Spinners
  }
}
</script>
<style lang="less" scoped>
  .experiment {
    width: 500px;
    height: 500px;
    margin: 0 auto;
    display: flex;
    justify-content: center;
  }
</style>