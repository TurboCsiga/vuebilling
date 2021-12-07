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
        <tr>
            <td><input type="text" v-model="title"></td>
            <td><input type="number" v-model="price"></td>
            <td><input type="number" v-model="quantity"></td>
            <td><button @click="hozzaad">Add</button></td>
        </tr>
  </div>
</template>

<script>
import Itemek from './Itemek.vue'

 export default {
    props: ['tetel'],
    components: { Itemek },

    data() {
        return {
            title: null,
            price: null,
            quantity: null
        }
    },
    methods: {
        hozzaad() {
            this.$emit("hozzaad", { title: this.title, price: this.price, quantity: this.quantity})
        }
    }
}
</script>

<style scoped>
    td{
        padding-right: 10px;
    }
    
</style>