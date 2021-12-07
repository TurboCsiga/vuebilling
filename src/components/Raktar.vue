<template>
  <div>
      <tr>
          <td>Title</td>
          <td>Price</td>
          <td>Quantity</td>
          <td>Operations</td>
      </tr>
      <itemek
            v-for="e in tetel"
            v-bind:key="e"
            :tetel = "e"
        />
  </div>
</template>

<script>
import Itemek from './Itemek.vue'

 export default {
    props: ['tetel'],
    components: { Itemek }
}
</script>

<style scoped>
    td{
        padding-right: 10px;
    }
    
</style>