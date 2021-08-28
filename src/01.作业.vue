<template>
  <div>
<h-table></h-table>
<h-table>
  <template v-slot:name="spoce">
<h4>帅气的：{{spoce.row}}</h4>
  </template>
  <template v-slot:age="spoce">
今年：{{spoce.row}}岁
  </template>
  <template v-slot:img="spoce">
<img :src="spoce.row" alt="">
  </template>

</h-table>
  </div>
</template>

<script>
import HTable from './components/01.h-table.vue'
export default {
  components: {
    HTable
  },
  data () {
    return {

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
