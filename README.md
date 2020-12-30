#安装
```
npm install @oldeng/v-spiners
```

#使用
```
import { Spinners } from "v-spinners";
import "v-spinners/plugin/v-spinners.css";
```
|  参数   | 值  | 作用 |
|  ----  | ----  |----|
| type  | 字符窜： small、middle、default | 设置spinners尺寸 |


#
#使用示例
```
<template>
  <div class="experiment">
    <div class="demo1">
      <v-spinners :type="type"></v-spinners>
    </div>
  </div>
</template>
<script>
// @ is an alias to /src
import { Spinners } from '../../plugin/v-spinners.umd';
import '../../plugin/v-spinners.css';

export default {
  name: 'experiment',
  data() {
    return {
      type: 'default'
    }
  },
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
```