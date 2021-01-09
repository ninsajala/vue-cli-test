<template>
  <form>
    <b>Add Item to Cart</b>
    <label for="name">Item</label>
    <input type="text" v-model="newItem.name" />

    <label for="price">Price</label>
    <input type="number" v-model="newItem.price" />

    <label for="amount">Amount</label>
    <input type="number" v-model="newItem.amount" />
    <button @click.prevent="addItem">Add</button>
  </form>
</template>

<script>
export default {
  props: {
    newItem: Object,
    addItem: Function,
  },
};
</script>

<style scope>
form {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}

button {
  width: auto;
  margin: 4px;
}
</style>
