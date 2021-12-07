<template>
  <div>
    <tr>
        <td>{{title}}</td>
        <td>{{price}}</td>
        <td>{{quantity}}</td>
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

</style>
