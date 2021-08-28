<template>
  <div
  class="my-header"
  :style="{backgroundColor, color}">
    {{ title }}
  </div>
</template>

<script>
export default {
  props: {
    // key 要接受的数据
    // 值 又是一个约束对象
    title: {
      // 约束的数据类型
      type: String,
      // 该数据为必传项
      required: true
    },
    backgroundColor: {
      type: String,
      // 设置默认值
      default: '#1d7bff'
    },
    color: {
      type: String,
      default: '#fff'
    }
  }
}
</script>

<style lang="less" scoped>
  .my-header {
    height: 45px;
    line-height: 45px;
    text-align: center;
    background-color: #1d7bff;
    color: #fff;
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    z-index: 2;
  }
</style>
