<template>
  <div>
      <tr>
          <th>Title</th>
          <th>Price</th>
          <th>Quantity</th>
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
    
</style>