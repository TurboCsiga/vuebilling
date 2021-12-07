<template>
  <div>
    <tr>
        <td>{{title}}</td>
        <td>{{price}}</td>
        <td>{{quantity}}</td>
        <td><button @click="torol">X</button><button>Edit</button></td>
    </tr>
    
  </div>
</template>

<script>
 export default {
    props: ['tetel'],
    data() {
        return {
            title: this.tetel.title,
            price: this.tetel.price,
            quantity: this.tetel.quantity
        }
    },
    methods:{
      torol() {
      this.$emit("torol", this.tetel.title)
    }
}
}

</script>

<style scoped>
  td{
        padding-right: 10px;
    }
</style>
