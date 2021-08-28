<template>
  <div>
    //头部
<MyHeader title="购物车"></MyHeader>
<MyTabBar :arr="tabList"></MyTabBar>
  </div>
</template>

<script>
import MyHeader from './components/MyHeader.vue'
import MyTabBar from './components/MyTabBar.vue'
export default {
  components: {
    MyHeader,
    MyTabBar
  },
  data () {
    return {
      tabList: [
        {
          iconText: 'icon-shangpinliebiao',
          text: '商品列表',
          componentName: 'MyGoodsList'
        },
        {
          iconText: 'icon-sousuo',
          text: '商品搜索',
          componentName: 'MyGoodsSearch'
        },
        {
          iconText: 'icon-user',
          text: '我的信息',
          componentName: 'MyUserInfo'
        }
      ]
    }
  },

  created () {

  },

  methods: {

  }
}
</script>

<style scoped>

</style>
