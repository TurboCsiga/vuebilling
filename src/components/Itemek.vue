<template>
  <div>
    <tr>
        <td>{{title}}</td>
        <td>{{price}}</td>
        <td>{{quantity}}</td>
        <td><button>X</button><button>Edit</button></td>
    </tr>
    <tr>
        <td><input type="text"></td>
        <td><input type="text"></td>
        <td><input type="text"></td>
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
    }
}
</script>

<style scoped>
  td{
        padding-right: 10px;
    }
</style>
