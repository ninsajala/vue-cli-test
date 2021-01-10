<template>
  <b-form>
    <b>Add Item to Cart</b>
    <label for="name">Item</label>
    <input class="input-small" size="sm" type="text" v-model="newItem.name" />

    <label for="price">Price</label>
    <input class="input-small" size="sm" type="number" v-model="newItem.price" />

    <label for="amount">Amount</label>
    <input class="input-small" size="sm" type="number" v-model="newItem.amount" />
    <b-button variant="outline-primary" @click.prevent="addItem"
    :disabled="!newItem.name.length || newItem.amount < 1 || newItem.price <= 0"
    >Add</b-button>
  </b-form>
</template>

<script>
export default {
  props: {
    newItem: Object,
    addItem: Function,
  },
};
</script>

<style scoped>
form {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  border: solid black 1px;
  padding: 5px;
  border-radius: 10px;
}

b-button {
  width: auto;
}

form input {
  text-align: center;
  margin-bottom: 5px !important;
  width: 100px;
}
</style>
