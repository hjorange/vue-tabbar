<template>
  <div class="my-tab-bar">
  <div @click="active=index" :class="{current:active===index }"  class="tab-item" v-for="(item,index) in arr" :key="item.iconText">
      <!-- 图标 -->
      <span class="iconfont" :class="item.iconText"></span>
      <!-- 文字 -->
      <span>{{item.text}}</span>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    arr: {
      type: Array,
      required: true,
      validator (value) {
        if (value.length >= 2 && value.length <= 5) {
          return true
        } return false
      }
    }
  },
  data () {
    return {
      active: ''
    }
  }
}
</script>

<style lang="less" scoped>
.my-tab-bar {
  position: fixed;
  left: 0;
  bottom: 0;
  width: 100%;
  height: 50px;
  border-top: 1px solid #ccc;
  display: flex;
  justify-content: space-around;
  align-items: center;
  background-color: white;
  .tab-item {
    display: flex;
    flex-direction: column;
    align-items: center;
  }
}

.current {
  color: #1d7bff;
}
</style>
